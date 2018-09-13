# Python OOP Patterns

## Sources
- [OOP Patterns on SourceMaking (great learning structure)](https://sourcemaking.com)
- [Python Patterns by Sakis Kasampalis (mostly useful)](https://github.com/faif/python-patterns/)
- [Article on patterns by Andrei Boyanov (wish there will be more)](https://www.toptal.com/python/python-design-patterns)
- [Python patterns by Brandon Rhodes (wicked cool)](http://python-patterns.guide)

## Contents
- [Creational patterns](#-creational-patterns)
    - [Abstract Factory](#-abstract-factory)
    - [Builder](#-builder)
    - [Factory Method](#-factory-method)
    - [Object Pool](#-object-pool)
    - [Prototype](#-prototype)
    - [Singleton](#-singleton)
- [Structural patterns](#-structural-patterns)
    - [Adapter](#-adapter)
    - [Bridge](#-bridge)
    - [Composite](#-composite)
    - [Decorator](#-decorator)
    - [Facade](#-facade)
    - [Flyweight](#-flyweight)
    - [Private Class Data](#-private-class-data)
    - [Proxy](#-proxy)
- [Behavioral patterns](#-behavioral-patterns)
    - [Chain of Responsibility](#-chain-of-responsibility)
    - [Command](#-command)
    - [Interpreter](#-interpreter)
    - [Iterator](#-iterator)
    - [Mediator](#-mediator)
    - [Memento](#-memento)
    - [Null Object](#-null-object)
    - [Observer](#-observer)
    - [State](#-state)
    - [Strategy](#-strategy)
    - [Template Method](#-template-method)
    - [Visitor](#-visitor)

***
## Creational patterns
1. Sometimes creational patterns are competitors:
    - There are cases when either Prototype or Abstract Factory could be used profitably
2. At other times they are complementary:
    - Abstract Factory might store a set of Prototypes from which to clone and return product objects
    - Builder can use one of the other patterns to implement which components get built
    - Abstract Factory, Builder, and Prototype can use Singleton in their implementation
3. Abstract Factory, Builder, and Prototype define a factory object that's responsible for knowing and creating the class of product objects, and make it a parameter of the system
    - Abstract Factory has the factory object producing objects of several classes
    - Builder has the factory object building a complex product incrementally using a correspondingly complex protocol
    - Prototype has the factory object (aka prototype) building a product by copying a prototype object.
4. Abstract Factory classes are often implemented with Factory Methods, but they can also be implemented using Prototype.
5. Abstract Factory can be used as an alternative to Facade to hide platform-specific classes.
6. Builder focuses on constructing a complex object step by step. Abstract Factory emphasizes a family of product objects (either simple or complex). Builder returns the product as a final step, but as far as the Abstract Factory is concerned, the product gets returned immediately.
7. Builder is to creation as Strategy is to algorithm.
8. Builder often builds a Composite.
9. Factory Methods are usually called within Template methods.
10. Factory Method: creation through inheritance. Prototype: creation through delegation.
11. Often, designs start out using Factory Method (less complicated, more customizable, subclasses proliferate) and evolve toward Abstract Factory, Prototype, or Builder (more flexible, more complex) as the designer discovers where more flexibility is needed.
12. Prototype doesn't require subclassing, but it does require an Initialize operation. Factory Method requires subclassing, but doesn't require Initialize.
13. Designs that make heavy use of the Composite and Decorator patterns often can benefit from Prototype as well.

***
### Abstract Factory
> Provides a way to encapsulate a group of individual factories.

In Java and other languages, the Abstract Factory Pattern serves to provide an interface for creating related/dependent objects without need to specify their actual class.

The idea is to abstract the creation of objects depending on business logic, platform choice, etc.

In Python we can simply use the class itself as that callable, because classes are first class objects in Python.

#### Intent
- Provide an interface for creating families of related or dependent objects without specifying their concrete classes
- A hierarchy that encapsulates: many possible "platforms", and the construction of a suite of "products"
- The `new` operator considered harmful

#### Example
```python
import random


class PetShop(object):
    def __init__(self, animal_factory=None):
        self.pet_factory = animal_factory

    def show_pet(self):
        pet = self.pet_factory()
        print("We have a lovely {}".format(pet))


class Dog(object):
    def speak(self):
        return "woof"


class Cat(object):
    def speak(self):
        return "meow"


# Additional factories:
def random_animal():
    return random.choice([Dog, Cat])()


cat_shop = PetShop(Cat)
cat_shop.show_pet()

# A shop that sells random animals
shop = PetShop(random_animal)
```
[Abstract Factory on SourceMaking](https://sourcemaking.com/design_patterns/abstract_factory/python/1)

***
### Builder

> It decouples the creation of a complex object and its representation, so that the same process can be reused to build objects from the same family.

This is useful when you must separate the specification of an object from its actual representation (generally for abstraction).

#### Intent
- Separate the construction of a complex object from its representation so that the same construction process can create different representations.
- Parse a complex representation, create one of several targets.

### Example
```python
class Builder(object):
    def __init__(self):
        self.building = None

    def new_building(self):
        self.building = Building()

    def build_floor(self):
        raise NotImplementedError

    def build_size(self):
        raise NotImplementedError


class BuilderHouse(Builder):
    def build_floor(self):
        self.building.floor = 'One'

    def build_size(self):
        self.building.size = 'Big'


class BuilderFlat(Builder):
    def build_floor(self):
        self.building.floor = 'More than One'

    def build_size(self):
        self.building.size = 'Small'


class Building(object):

    def __init__(self):
        self.floor = None
        self.size = None

    def __repr__(self):
        return 'Floor: {0.floor} | Size: {0.size}'.format(self)


def construct_building(builder):
    builder.new_building()
    builder.build_floor()
    builder.build_size()
    return builder.building

building = construct_building(BuilderHouse())
building = construct_building(BuilderFlat())
```

[Builder on SourceMaking](https://sourcemaking.com/design_patterns/builder/python/1)

***
### Factory Method
> Creates objects without having to specify the exact class.

The Factory Method pattern can be used to create an interface for a method, leaving the implementation to the class that gets instantiated.

The Factory Method can be seen in the popular web framework Django: http://django.wikispaces.asu.edu/*NEW*+Django+Design+Patterns For example, in a contact form of a web page, the subject and the message fields are created using the same form factory (CharField()), even though they have different implementations according to their
purposes.

#### Intent
- Define an interface for creating an object, but let subclasses decide which class to instantiate. Factory Method lets a class defer instantiation to subclasses.
- Defining a "virtual" constructor.
- The `new` operator considered harmful.


#### Example
```python
class GreekGetter(object):
    """A simple localizer a la gettext"""

    def __init__(self):
        self.trans = dict(dog="σκύλος", cat="γάτα")

    def get(self, msgid):
        """We'll punt if we don't have a translation"""
        return self.trans.get(msgid, str(msgid))


class EnglishGetter(object):
    """Simply echoes the msg ids"""

    def get(self, msgid):
        return str(msgid)


def get_localizer(language="English"):
    """The factory method"""
    languages = dict(English=EnglishGetter, Greek=GreekGetter)
    return languages[language]()


e, g = get_localizer(language="English"), get_localizer(language="Greek")
# Localize some text
for msgid in "dog parrot cat bear".split():
    print(e.get(msgid), g.get(msgid))
```

[About Factory Method by Brandon Rhodes](http://python-patterns.guide/gang-of-four/factory-method/)

***
### Object Pool
> Object pooling can offer a significant performance boost; it is most effective in situations where the cost of initializing a class instance is high, the rate of instantiation of a class is high, and the number of instantiations in use at any one time is low.

A pool allows to 'check out' an inactive object and then to return it. If none are available the pool creates one to provide without wait.

Stores a set of initialized objects kept ready to use.

#### Example
```python
class ReusablePool:
    """Manage Reusable objects for use by Client objects."""

    def __init__(self, size):
        self._reusables = [Reusable() for _ in range(size)]

    def acquire(self):
        return self._reusables.pop()

    def release(self, reusable):
        self._reusables.append(reusable)


class Reusable:
    """
    Collaborate with other objects for a limited amount of time, then
    they are no longer needed for that collaboration.
    """


def main():
    reusable_pool = ReusablePool(10)
    reusable = reusable_pool.acquire()
    reusable_pool.release(reusable)

main()
```

***
### Prototype

> Creates new object instances by cloning prototype.

#### Intent
- Specify the kinds of objects to create using a prototypical instance, and create new objects by copying this prototype.
- Co-opt one instance of a class for use as a breeder of all future instances.
- The new operator considered harmful.

#### Example
```python
class Prototype(object):
    value = 'default'

    def clone(self, **attrs):
        """Clone a prototype and update inner attributes dictionary"""
        obj = self.__class__()
        obj.__dict__.update(attrs)
        return obj

prototype = Prototype()

d = prototype.clone()
a = prototype.clone(value='a-value', category='a')
```

Another one from SourceMaking
```python
import copy

class Prototype:
    """Example class to be copied."""

prototype = Prototype()
prototype_copy = copy.deepcopy(prototype)
```

***
### Singleton
> The Singleton pattern is used when we want to guarantee that only one instance of a given class exists during runtime. Can be replaced with dependency injection

#### Intent
- Ensure a class has only one instance, and provide a global point of access to it.
- Encapsulated "just-in-time initialization" or "initialization on first use".

### Example
```python
class Logger(object):
    def __new__(cls, *args, **kwargs):
        if not hasattr(cls, '_logger'):
            cls._logger = super(Logger, cls).__new__(cls, *args, **kwargs)
        return cls._logger
```

With metaclass
```python
class Singleton(type):
    """
    Define an Instance operation that lets clients access its unique
    instance.
    """

    def __init__(cls, name, bases, attrs, **kwargs):
        super().__init__(name, bases, attrs)
        cls._instance = None

    def __call__(cls, *args, **kwargs):
        if cls._instance is None:
            cls._instance = super().__call__(*args, **kwargs)
        return cls._instance


class MyClass(object):
    __metaclass__ = Singleton
```

These are the alternatives to using a Singleton in Python:
- Use a module.
- Create one instance somewhere at the top-level of your application, perhaps in the config file.
- Pass the instance to every object that needs it. That’s a dependency injection and it’s a powerful and easily mastered mechanism.

***
## Structural patterns
- Adapter makes things work after they're designed; Bridge makes them work before they are.
- Bridge is designed up-front to let the abstraction and the implementation vary independently. Adapter is retrofitted to make unrelated classes work together.
- Adapter provides a different interface to its subject. Proxy provides the same interface. Decorator provides an enhanced interface.
- Adapter changes an object's interface, Decorator enhances an object's responsibilities. Decorator is thus more transparent to the client. As a consequence, Decorator supports recursive composition, which isn't possible with pure Adapters.
- Composite and Decorator have similar structure diagrams, reflecting the fact that both rely on recursive composition to organize an open-ended number of objects.
- Composite can be traversed with Iterator. Visitor can apply an operation over a Composite. Composite could use Chain of responsibility to let components access global properties through their parent. It could also use Decorator to override these properties on parts of the composition. It could use Observer to tie one object structure to another and State to let a component change its behavior as its state changes.
- Composite can let you compose a Mediator out of smaller pieces through recursive composition.
- Decorator lets you change the skin of an object. Strategy lets you change the guts.
- Decorator is designed to let you add responsibilities to objects without subclassing. Composite's focus is not on embellishment but on representation. These intents are distinct but complementary. Consequently, Composite and Decorator are often used in concert.
- Decorator and Proxy have different purposes but similar structures. Both describe how to provide a level of indirection to another object, and the implementations keep a reference to the object to which they forward requests.
- Facade defines a new interface, whereas Adapter reuses an old interface. Remember that Adapter makes two existing interfaces work together as opposed to defining an entirely new one.
- Facade objects are often Singleton because only one Facade object is required.
- Mediator is similar to Facade in that it abstracts functionality of existing classes. Mediator abstracts/centralizes arbitrary communication between colleague objects, it routinely "adds value", and it is known/referenced by the colleague objects. In contrast, Facade defines a simpler interface to a subsystem, it doesn't add new functionality, and it is not known by the subsystem classes.
- Abstract Factory can be used as an alternative to Facade to hide platform-specific classes.
- Whereas Flyweight shows how to make lots of little objects, Facade shows how to make a single object represent an entire subsystem.
- Flyweight is often combined with Composite to implement shared leaf nodes.
- Flyweight explains when and how State objects can be shared.

***
### Adapter
> Allows the interface of an existing class to be used as another interface.

Facades used for interface simplfications, whereis  Adapters are al about altering the interface. Like using a cow when the system is expecting a duck.

#### Intent
- Convert the interface of a class into another interface clients expect. Adapter lets classes work together that couldn't otherwise because of incompatible interfaces.
- Wrap an existing class with a new interface.
- Impedance match an old component to a new system

#### Example
```python
import socket

def log(message, destination):
    destination.write('[{}] - {}'.format(datetime.now(), message))


class SocketWriter(object):

    def __init__(self, ip, port):
        self._socket = socket.socket(socket.AF_INET,
                                     socket.SOCK_DGRAM)
        self._ip = ip
        self._port = port

    def write(self, message):
        self._socket.send(message, (self._ip, self._port))

def log(message, destination):
    destination.write('[{}] - {}'.format(datetime.now(), message))

upd_logger = SocketWriter('1.2.3.4', '9999')
log('Something happened', udp_destination)
```
### Bridge
#### Intent
- Decouple an abstraction from its implementation so that the two can vary independently.
- Publish interface in an inheritance hierarchy, and bury implementation in its own inheritance hierarchy.
- Beyond encapsulation, to insulation

#### Example
```python
class DrawingAPI1(object):
    def draw_circle(self, x, y, radius):
        print('API1.circle at {}:{} radius {}'.format(x, y, radius))


class DrawingAPI2(object):
    def draw_circle(self, x, y, radius):
        print('API2.circle at {}:{} radius {}'.format(x, y, radius))


class CircleShape(object):
    def __init__(self, x, y, radius, drawing_api):
        self._x = x
        self._y = y
        self._radius = radius
        self._drawing_api = drawing_api

    # low-level i.e. Implementation specific
    def draw(self):
        self._drawing_api.draw_circle(self._x, self._y, self._radius)

    # high-level i.e. Abstraction specific
    def scale(self, pct):
        self._radius *= pct


shapes = (
    CircleShape(1, 2, 3, DrawingAPI1()),
    CircleShape(5, 7, 11, DrawingAPI2())
)

for shape in shapes:
    shape.scale(2.5)
    shape.draw()

main()
```
[Bridge on SourceMaking](https://sourcemaking.com/design_patterns/bridge/python/1)

***
### Composite
> Describes a group of objects that is treated as a single instance.

#### Intent
- Compose objects into tree structures to represent whole-part hierarchies. Composite lets clients treat individual objects and compositions of objects uniformly.
- Recursive composition
- "Directories contain entries, each of which could be a directory."
- 1-to-many "has a" up the "is a" hierarchy

#### Example
```python
class Graphic:
    def render(self):
        raise NotImplementedError("You should implement this.")


class CompositeGraphic(Graphic):
    def __init__(self):
        self.graphics = []

    def render(self):
        for graphic in self.graphics:
            graphic.render()

    def add(self, graphic):
        self.graphics.append(graphic)

    def remove(self, graphic):
        self.graphics.remove(graphic)


class Ellipse(Graphic):
    def __init__(self, name):
        self.name = name

    def render(self):
        print("Ellipse: {}".format(self.name))


if __name__ == '__main__':
    ellipse1 = Ellipse("1")
    ellipse2 = Ellipse("2")
    ellipse3 = Ellipse("3")
    ellipse4 = Ellipse("4")

    graphic1 = CompositeGraphic()
    graphic2 = CompositeGraphic()

    graphic1.add(ellipse1)
    graphic1.add(ellipse2)
    graphic1.add(ellipse3)
    graphic2.add(ellipse4)

    graphic = CompositeGraphic()

    graphic.add(graphic1)
    graphic.add(graphic2)

graphic.render()
```

[Composite Pattern at SourceMaking](https://sourcemaking.com/design_patterns/composite/python/1)
[On composite pattern by Brandon Rhodes](http://python-patterns.guide/gang-of-four/composite/)

***
### Decorator
> Adds behaviour to object without affecting its class.

#### Intent
- Attach additional responsibilities to an object dynamically. Decorators provide a flexible alternative to subclassing for extending functionality.
- Client-specified embellishment of a core object by recursively wrapping it.
- Wrapping a gift, putting it in a box, and wrapping the box.

#### Example
```python
class TextTag(object):
    def __init__(self, text):
        self._text = text

    def render(self):
        return self._text


class BoldWrapper(TextTag):
    """Wraps a tag in <b>"""
    def __init__(self, wrapped):
        self._wrapped = wrapped

    def render(self):
        return "<b>{}</b>".format(self._wrapped.render())


class ItalicWrapper(TextTag):
    """Wraps a tag in <i>"""
    def __init__(self, wrapped):
        self._wrapped = wrapped

    def render(self):
        return "<i>{}</i>".format(self._wrapped.render())

simple_hello = TextTag("hello, world!")
special_hello = ItalicWrapper(BoldWrapper(simple_hello))
```

[Decorator at SourceMaking](https://sourcemaking.com/design_patterns/decorator/python/1)
[Thoughts on Decorator pattern by Brandon Rhodes](http://python-patterns.guide/gang-of-four/decorator-pattern/)

***
### Facade
> Provides a simpler unified interface to a complex system

It provides an easier way to access functions of the underlying system by providing a single entry point. This kind of abstraction is seen in many real life situations. For example, we can turn on a computer by just pressing a button, but in fact there are many procedures and operations done when that happens (e.g., loading programs from disk to memory). In this case, the button serves as an unified interface to all the underlying procedures to turn on a computer.

#### Intent

Facade is an elegant Python design pattern. It's a perfect way of streamlining the interface. Facades used for interface simplfications, whereis  Adapters are al about altering the interface.

#### Example
```python
class Car(object):

    def __init__(self):
        self._tyres = [
            Tyre('front_left'),
            Tyre('front_right'),
            Tyre('rear_left'),
            Tyre('rear_right'), ]
        self._tank = Tank(70)

    def tyres_pressure(self):
        return [tyre.pressure for tyre in self._tyres]

    def fuel_level(self):
        return self._tank.level
```

***
### Flyweight
> Minimizes memory usage by sharing data with other similar objects.

#### Intent
- Use sharing to support large numbers of fine-grained objects efficiently.
- The Motif GUI strategy of replacing heavy-weight widgets with light-weight gadgets.

#### Example
```python
import abc


class FlyweightFactory:
    """
    Create and manage flyweight objects.
    Ensure that flyweights are shared properly. When a client requests a
    flyweight, the FlyweightFactory object supplies an existing instance
    or creates one, if none exists.
    """
    def __init__(self):
        self._flyweights = {}

    def get_flyweight(self, key):
        try:
            flyweight = self._flyweights[key]
        except KeyError:
            flyweight = ConcreteFlyweight()
            self._flyweights[key] = flyweight
        return flyweight


class Flyweight(metaclass=abc.ABCMeta):
    """
    Declare an interface through which flyweights can receive and act on
    extrinsic state.
    """
    def __init__(self):
        self.intrinsic_state = None

    @abc.abstractmethod
    def operation(self, extrinsic_state):
        pass


class ConcreteFlyweight(Flyweight):
    """
    Implement the Flyweight interface and add storage for intrinsic
    state, if any. A ConcreteFlyweight object must be sharable. Any
    state it stores must be intrinsic; that is, it must be independent
    of the ConcreteFlyweight object's context.
    """

    def operation(self, extrinsic_state):
        pass


flyweight_factory = FlyweightFactory()
concrete_flyweight = flyweight_factory.get_flyweight("key")
concrete_flyweight.operation(None)
```

***
### Private Class Data
> Control write access to class attributes

#### Intent
- Control write access to class attributes
- Separate data from methods that use it
- Encapsulate class data initialization

#### Example
```python
class DataClass:
    """Hide all the attributes."""
    def __init__(self):
        self.value = None

    def __get__(self, instance, owner):
        return self.value

    def __set__(self, instance, value):
        if self.value is None:
            self.value = value


class MainClass:
    """Initialize data class through the data class's constructor."""
    attribute = DataClass()

    def __init__(self, value):
        self.attribute = value


m = MainClass(True)
m.attribute = False
```

Restrict what methods of the wrapped classs to expose
```python
class User:
    _persist_methods = ['get', 'save', 'delete']

    def __init__(self, persister):
        self._persister = persister

    def __getattr__(self, attribute):
        if attribute in self._persist_methods:
            return getattr(self._persister, attribute)
```

***
### Proxy
> Provide a surrogate or placeholder for another object to control access to it or add other responsibilities.

#### Intent
- Provide a surrogate or placeholder for another object to control access to it.
- Use an extra level of indirection to support distributed, controlled, or intelligent access.
- Add a wrapper and delegation to protect the real component from undue complexity.

#### Example
```python
import abc


class Subject(metaclass=abc.ABCMeta):
    @abc.abstractmethod
    def request(self):
        pass


class Proxy(Subject):
    """
    Maintain a reference that lets the proxy access the real subject.
    Provide an interface identical to Subject's.
    """
    def __init__(self, real_subject):
        self._real_subject = real_subject

    def request(self):
        # ...
        self._real_subject.request()
        # ...


class RealSubject(Subject):
    """Define the real object that the proxy represents."""
    def request(self):
        pass


real_subject = RealSubject()
proxy = Proxy(real_subject)
proxy.request()
```

***
## Behavioral patterns
- Behavioral patterns are concerned with the assignment of responsibilities between objects, or, encapsulating behavior in an object and delegating requests to it.
- Chain of responsibility, Command, Mediator, and Observer, address how you can decouple senders and receivers, but with different trade-offs. Chain of responsibility passes a sender request along a chain of potential receivers. Command normally specifies a sender-receiver connection with a subclass. Mediator has senders and receivers reference each other indirectly. Observer defines a very decoupled interface that allows for multiple receivers to be configured at run-time.
- Chain of responsibility can use Command to represent requests as objects.
- Chain of responsibility is often applied in conjunction with Composite. There, a component's parent can act as its successor.
- Command and Memento act as magic tokens to be passed around and invoked at a later time. In Command, the token represents a request; in Memento, it represents the internal state of an object at a particular time. Polymorphism is important to Command, but not to Memento because its interface is so narrow that a memento can only be passed as a value.
- Command can use Memento to maintain the state required for an undo operation.
- MacroCommands can be implemented with Composite.
- A Command that must be copied before being placed on a history list acts as a Prototype.
- Interpreter can use State to define parsing contexts.
- The abstract syntax tree of Interpreter is a Composite (therefore Iterator and Visitor are also applicable).
- Terminal symbols within Interpreter's abstract syntax tree can be shared with Flyweight.
- Iterator can traverse a Composite. Visitor can apply an operation over a Composite.
- Polymorphic Iterators rely on Factory Methods to instantiate the appropriate Iterator subclass.
- Mediator and Observer are competing patterns. The difference between them is that Observer distributes communication by introducing "observer" and "subject" objects, whereas a Mediator object encapsulates the communication between other objects. We've found it easier to make reusable Observers and Subjects than to make reusable Mediators.
- On the other hand, Mediator can leverage Observer for dynamically registering colleagues and communicating with them.
- Mediator is similar to Facade in that it abstracts functionality of existing classes. Mediator abstracts/centralizes arbitrary communication between colleague objects, it routinely "adds value", and it is known/referenced by the colleague objects (i.e. it defines a multidirectional protocol). In contrast, Facade defines a simpler interface to a subsystem, it doesn't add new functionality, and it is not known by the subsystem classes (i.e. it defines a unidirectional protocol where it makes requests of the subsystem classes but not vice versa).
- Memento is often used in conjunction with Iterator. An Iterator can use a Memento to capture the state of an iteration. The Iterator stores the Memento internally.
- State is like Strategy except in its intent.
- Flyweight explains when and how State objects can be shared.
- State objects are often Singletons.
- Strategy lets you change the guts of an object. Decorator lets you change the skin.
- Strategy is to algorithm. as Builder is to creation.
- Strategy has 2 different implementations, the first is similar to State. The difference is in binding times (Strategy is a bind-once pattern, whereas State is more dynamic).
- Strategy objects often make good Flyweights.
- Strategy is like Template method except in its granularity.
- Template method uses inheritance to vary part of an algorithm. Strategy uses delegation to vary the entire algorithm.
- The Visitor pattern is like a more powerful Command pattern because the visitor may initiate whatever is appropriate for the kind of object it encounters.

***
### Chain of Responsobility
> 

#### Intent
- Avoid coupling the sender of a request to its receiver by giving more than one object a chance to handle the request. Chain the receiving objects and pass the request along the chain until an object handles it.
- Launch-and-leave requests with a single processing pipeline that contains many possible handlers.
- An object-oriented linked list with recursive traversal.

This pattern gives us a way to treat a request using different methods, each one addressing a specific part of the request. You know, one of the best principles for good code is the Single Responsibility principle.

_Every piece of code must do one, and only one, thing._

This principle is deeply integrated in this design pattern.

#### Example
```python
class ContentFilter(object):
    def __init__(self, filters=None):
        self._filters = list()
        if filters is not None:
            self._filters += filters

    def filter(self, content):
        for filter in self._filters:
            content = filter(content)
        return content

filter = ContentFilter([
                offensive_filter,
                ads_filter,
                porn_video_filter])
filtered_content = filter.filter(content)
```
[Chain of Responsibility at SourceMaking](https://sourcemaking.com/design_patterns/chain_of_responsibility/python/1)

***
### Command
> Encapsulates all information needed to perform an action or trigger an event.

#### Intent
- Encapsulate a request as an object, thereby letting you parametrize clients with different requests, queue or log requests, and support undoable operations.
- Promote "invocation of a method on an object" to full object status
- An object-oriented callback

The command pattern is handy in situations when, for some reason, we need to start by preparing what will be executed and then to execute it when needed. The advantage is that encapsulating actions in such a way enables Python developers to add additional functionalities related to the executed actions, such as undo/redo, or keeping a history of actions and the like.

#### Example
```python
class RenameFileCommand(object):
    def __init__(self, from_name, to_name):
        self._from = from_name
        self._to = to_name

    def execute(self):
        os.rename(self._from, self._to)

    def undo(self):
        os.rename(self._to, self._from)

class History(object):
    def __init__(self):
        self._commands = list()

    def execute(self, command):
        self._commands.append(command)
        command.execute()

    def undo(self):
        self._commands.pop().undo()

history = History()
history.execute(RenameFileCommand('docs/cv.doc', 'docs/cv-en.doc'))
history.execute(RenameFileCommand('docs/cv1.doc', 'docs/cv-bg.doc'))
history.undo()
history.undo()
```

```python
class Command:

    def __init__(self, authenticate=None, authorize=None):
        self.authenticate = authenticate or self._not_authenticated
        self.authorize = authorize or self._not_autorized

    def execute(self, user, action):
        self.authenticate(user)
        self.authorize(user, action)
        return action()

command = Command()
if in_sudo_mode:
    command.authenticate = always_authenticated
    command.authorize = always_authorized
else:
    command.authenticate = config.authenticate
    command.authorize = config.authorize

command.execute(current_user, delete_user_action)
```

***
### Iterator
Iterators are built into Python. This is one of the most powerful characteristics of the language.

> Provide a way to access the elements of an aggregate objects equentially without exposing its underlying representation.

#### Intent
- Provide a way to access the elements of an aggregate object sequentially without exposing its underlying representation.
- The C++ and Java standard library abstraction that makes it possible to decouple collection classes and algorithms.
- Promote to "full object status" the traversal of a collection.
- Polymorphic traversal

#### Example
```python
import collections.abc


class ConcreteAggregate(collections.abc.Iterable):
    def __init__(self):
        self._data = None

    def __iter__(self):
        return ConcreteIterator(self)


class ConcreteIterator(collections.abc.Iterator):
    """Implement the Iterator interface."""
    def __init__(self, concrete_aggregate):
        self._concrete_aggregate = concrete_aggregate

    def __next__(self):
        if True:  # if no_elements_to_traverse:
            raise StopIteration
        return None  # return element


concrete_aggregate = ConcreteAggregate()
for _ in concrete_aggregate:
    pass
```

***
### Mediator
> Encapsulates how a set of objects interact.

#### Intent
- Define an object that encapsulates how a set of objects interact. Mediator promotes loose coupling by keeping objects from referring to each other explicitly, and it lets you vary their interaction independently.
- Design an intermediary to decouple many peers.
- Promote the many-to-many relationships between interacting peers to "full object status".

#### Example
```python
class Mediator:
    """
    Implement cooperative behavior by coordinating Colleague objects.
    Know and maintains its colleagues.
    """
    def __init__(self):
        self._colleague_1 = Colleague1(self)
        self._colleague_2 = Colleague2(self)


class Colleague1:
    """
    Know its Mediator object.
    Communicate with its mediator whenever it would have otherwise
    communicated with another colleague.
    """
    def __init__(self, mediator):
        self._mediator = mediator


class Colleague2:
    """
    Know its Mediator object.
    Communicate with its mediator whenever it would have otherwise
    communicated with another colleague.
    """
    def __init__(self, mediator):
        self._mediator = mediator

mediator = Mediator()
```

***
### Memento
> Provides the ability to restore an object to its previous state.

#### Intent
- Without violating encapsulation, capture and externalize an object's internal state so that the object can be returned to this state later.
- A magic cookie that encapsulates a "check point" capability.
- Promote undo or rollback to full object status.

#### Example
```python
import pickle


class Originator:
    """
    Create a memento containing a snapshot of its current internal state.
    Use the memento to restore its internal state.
    """
    def __init__(self):
        self._state = None

    def set_memento(self, memento):
        previous_state = pickle.loads(memento)
        vars(self).clear()
        vars(self).update(previous_state)

    def create_memento(self):
        return pickle.dumps(vars(self))


originator = Originator()
memento = originator.create_memento()
originator._state = True
originator.set_memento(memento)
```

### Null Object
> Encapsulate the absence of an object by providing a substitutable alternative that offers suitable default do nothing behavior

#### Intent
The intent of a Null Object is to encapsulate the absence of an object by providing a substitutable alternative that offers suitable default do nothing behavior. In short, a design where "nothing will come of nothing"

Use the Null Object pattern when

- an object requires a collaborator. The Null Object pattern does not introduce this collaboration--it makes use of a collaboration that already exists
- some collaborator instances should do nothing
- you want to abstract the handling of null away from the client


#### Example
```python
import abc


class AbstractObject(metaclass=abc.ABCMeta):
    @abc.abstractmethod
    def request(self):
        pass


class RealObject(AbstractObject):
    def request(self):
        pass


class NullObject(AbstractObject):
    def request(self):
        pass
```

***
### Observer
> Maintains a list of dependents and notifies them of any state changes.

#### Intent
- Define a one-to-many dependency between objects so that when one object changes state, all its dependents are notified and updated automatically.
- Encapsulate the core (or common or engine) components in a Subject abstraction, and the variable (or optional or user interface) components in an Observer hierarchy.
- The "View" part of Model-View-Controller.

#### Example
```python
import abc


class Subject:
    """
    Know its observers. Any number of Observer objects may observe a subject.
    Send a notification to its observers when its state changes.
    """
    def __init__(self):
        self._observers = set()
        self._subject_state = None

    def attach(self, observer):
        observer._subject = self
        self._observers.add(observer)

    def detach(self, observer):
        observer._subject = None
        self._observers.discard(observer)

    def _notify(self):
        for observer in self._observers:
            observer.update(self._subject_state)

    @property
    def subject_state(self):
        return self._subject_state

    @subject_state.setter
    def subject_state(self, arg):
        self._subject_state = arg
        self._notify()


class Observer(metaclass=abc.ABCMeta):
    """Define an updating interface for objects that should be notified of changes in a subject."""
    def __init__(self):
        self._subject = None
        self._observer_state = None

    @abc.abstractmethod
    def update(self, arg):
        pass


class ConcreteObserver(Observer):
    """
    Implement the Observer updating interface to keep its state consistent with the subject's.
    Store state that should stay consistent with the subject's.
    """
    def update(self, arg):
        self._observer_state = arg
        # ...

subject = Subject()
concrete_observer = ConcreteObserver()
subject.attach(concrete_observer)
subject.subject_state = 123
```

***
### State
> Allow an object to alter its behavior when its internal state changes.

#### Intent
- Allow an object to alter its behavior when its internal state changes. The object will appear to change its class.
- An object-oriented state machine
- wrapper + polymorphic wrappee + collaboration

#### Example
```python
import abc


class Context:
    """
    Define the interface of interest to clients.
    Maintain an instance of a ConcreteState subclass that defines the current state.
    """
    def __init__(self, state):
        self._state = state

    def request(self):
        self._state.handle()


class State(metaclass=abc.ABCMeta):
    """Define an interface for encapsulating the behavior associated with a particular state of the Context."""
    @abc.abstractmethod
    def handle(self):
        pass


class ConcreteStateA(State):
    """Implement a behavior associated with a state of the Context."""
    def handle(self):
        pass


class ConcreteStateB(State):
    """Implement a behavior associated with a state of the Context."""
    def handle(self):
        pass


concrete_state_a = ConcreteStateA()
context = Context(concrete_state_a)
context.request()
```

***
### Strategy
> Enables selecting an algorithm at runtime.

#### Intent
- Define a family of algorithms, encapsulate each one, and make them interchangeable. Strategy lets the algorithm vary independently from the clients that use it.
- Capture the abstraction in an interface, bury implementation details in derived classes.

#### Example
```python
import types


class StrategyExample:

    def __init__(self, func=None):
        self.name = 'Strategy Example 0'
        if callable(func):
            # makes function a class metod
            self.execute = types.MethodType(func, self)

    def execute(self):
        print(self.name)


def execute_replacement1(self):
    print(self.name + ' from execute 1')


def execute_replacement2(self):
    print(self.name + ' from execute 2')


strat0 = StrategyExample()

strat1 = StrategyExample(execute_replacement1)
strat1.name = 'Strategy Example 1'

strat2 = StrategyExample(execute_replacement2)
strat2.name = 'Strategy Example 2'

strat0.execute()
strat1.execute()
strat2.execute()
```

[Strategy Example at SourceMaking](https://sourcemaking.com/design_patterns/strategy/python/1)

***
### Template Method
> Defines the skeleton of an algorithm, deferring steps to subclasses.

#### Intent
- Define the skeleton of an algorithm in an operation, deferring some steps to client subclasses. Template Method lets subclasses redefine certain steps of an algorithm without changing the algorithm's structure.
- Base class declares algorithm 'placeholders', and derived classes implement the placeholders.

#### Example
```python
import abc


class AbstractClass(metaclass=abc.ABCMeta):
    """
    Define abstract primitive operations that concrete subclasses define
    to implement steps of an algorithm.
    Implement a template method defining the skeleton of an algorithm.
    The template method calls primitive operations as well as operations
    defined in AbstractClass or those of other objects.
    """
    def template_method(self):
        self._primitive_operation_1()
        self._primitive_operation_2()

    @abc.abstractmethod
    def _primitive_operation_1(self):
        pass

    @abc.abstractmethod
    def _primitive_operation_2(self):
        pass


class ConcreteClass(AbstractClass):
    """
    Implement the primitive operations to carry out
    subclass-specificsteps of the algorithm.
    """
    def _primitive_operation_1(self):
        pass

    def _primitive_operation_2(self):
        pass


concrete_class = ConcreteClass()
concrete_class.template_method()
```

***
### Visitor
> Separates an algorithm from an object structure on which it operates.

#### Intent
- Represent an operation to be performed on the elements of an object structure. Visitor lets you define a new operation without changing the classes of the elements on which it operates.
- The classic technique for recovering lost type information.
- Do the right thing based on the type of two objects.
- Double dispatch

#### Example
```python
class Node(object):
    pass


class A(Node):
    pass


class B(Node):
    pass


class C(A, B):
    pass


class Visitor(object):

    def visit(self, node, *args, **kwargs):
        meth = None
        for cls in node.__class__.__mro__:
            meth_name = 'visit_' + cls.__name__
            meth = getattr(self, meth_name, None)
            if meth:
                break

        if not meth:
            meth = self.generic_visit
        return meth(node, *args, **kwargs)

    def generic_visit(self, node, *args, **kwargs):
        print('generic_visit ' + node.__class__.__name__)

    def visit_B(self, node, *args, **kwargs):
        print('visit_B ' + node.__class__.__name__)


visitor = Visitor()
visitor.visit(A())  # generic_visit A
visitor.visit(B())  # visit_B B
visitor.visit(C())  # visit_B C
```