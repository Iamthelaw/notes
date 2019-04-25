# Code complete notes

## TLDR part

The book is mostly outdated and contains some really crazy detailed chapters about
naming integer variables and placing spaces around block of code (layout).

But noneless it is a fundamental book for programming practices and a lot of things
that seem like they are obvious or always be there. Also the author is aware about "Extreme Programming" book and poke at it sometimes, and quotes a lot other fundamental
books like "The Practical Programmer" and "The Mythical Man-Month".

What I really like is a central motive of the whole book - as a programmer your
responsibility is **reduce complexity** of the software, not the other way around.
Classes and functions and good variable names are your tool to make code clear and
simple.

Short overview of chapters that I think worth reading is next.

### Chapter 3 Upstream prerequisites

This is about how changes in the software are cost more and more after the time and
the solution is to spend a lot of time analyzing prerequisites and by that saving
time and money in the future.

### Chapter 5 Software Design

What it is, levels of design, designing blocks and best practices. Pretty solid
stuff, I think this one is one of the good chapters and I took a lot notes from
there. But basic thought I think that there is a levels and practices but in the
end of the day design is hard, and good design is never the first attempt
to solve the problem.

### Chapter 6 Classes

How to write good abstractions, interfaces and inheritance and what are the "Bad"
classes. Lots of C++, Visual Basic and Java examples that is pretty hard to
convert to Python. In this book Python is a simple, a little dumb and slow language.

### Chapter 7 Routines

The whole book it is a confusing like hell name "routine" is just a synonim of
function or method. But, what I did liked that he clearly separating "routine""
from "procedure". Procedure is not returning anything, it is just running
commands in a specific order. Most of the chapter however is boring rules for
how to name "routine", how many parameters is bad, how to keep cohesion between
"routines" under control.

### Chapter 8 Defensive programming

That's about practices that programmers invented to make the code super defensive
agains user input, because users can use your software in a very unexpected ways.
Using assertions, sanitizing inputs, error handling etc. There is a tradeoff -
the more defensive programm is the more complex and bloated with checks it is.

### Chapter 9 Pseudocode programming process

Really enjoyed this one. He talks about how programmers can use PPP to try different
software designs quickly, how reviewing pseudocode is so much easier and simle then
actual code and that one of the great benefits of PPP is that it will be converted
to docstrings and comments after code is written.

### Chapter 11 Variable names

The boring one, but a little more entertaining then chapter about placing
spaces and new lines to organize code. Some good examples of bad names like
`ttl5`, `ttlS` and `tt1S`. Plus subchapter about naming conventions, and naming
conventions are pretty important in heavy specialized projects.

### Chapters 12-19 Data types, conditionals, loops

### Chapter 20 Software quality

So there is a quality that user think of and there is a quality of product that
programmers are think of. And they are not the same. So programmers can raise
software quality by doing code reviews, unit tests, prototyping,
design reviews, integration and system tests. And again for the author the main
reason to kepp software qulity high is to escape future changes of the software
that will cost more and more money. So next few chapters about quality practices.

### Chapter 21 Collaborative Construction

Code reviews, introspections and pair programming. He is not a fan of fulltime
pair programming and his idea of code reviews is pretty old - basically it is a
meeting when 2 or more reviwers are reading author code before meeting, making
notes and then gathering - author, reviwers and moderator to discuss code and
create a resulting paper of the founded bugs.

### Chapter 22 Developer Testing

Different testing practices and testing goals. What was interesting is a testing
notes and in later chapters he wrote about database of defects (say stackoverflow).
Some good tips to try out when writing test case, because most of tests that
programmers writing are positive tests, where the tests is a tool to find bugs.

### Chapter 23 Debugging

Practices to efficently debug to the core of the problem, brute force technics and
tips. But overall debugging is discouraged and a last resort. Author thinks that
good programmer should use his own mind to figure out the problem first and not
rush into hacking his way around.

### Chapter 24 Refactoring

The interesting thought is that refactoring (as it defined by the most respected
writers in this area Fowler) is making working code beautiful. It is not ment to
be used as a tool to fix bugs. If class is buggy, it shoud be rewritten from scratch
with a good design in mind. Refactoring is a cosmetics, not a suergery operation.

### Chapter 25-26 Code-tuning

Performance optimizations and traidoffs. The performance optimizations is highly
bad idea without proper measuring and knowing what you are doing. First write
clean readable and slow code, if it ever will be needed it can be optimized later
in exchange of readablilty.

### Chapter 27 Project size

Lots of numbers and stadies about the correlation between project size, team size
and quality of the software.

### Chapter 28 Managing construction

The role of the manager in the software construction - estimating project and treating
programmers like a people.

### Chapter 29 Integration

Chapter about how to ingrate parts of the bigger project if saw two teams are building
two big parts and the third is doing lots of smaller parts, combining techniques.
I think with microservices the problem is not going anywhere because different
teams can create not 100% compatible interfaces, miscomunicaion is a thing
in our days too.

### Chapter 30 Tool-oriented environments

Pretty good idea to before starting working on the project to make time to think
about what internal tool we would need to be efficent when working on this project.
It is a scaffolding scripts and local testing endpoints and CLI tools.

### Chapter 31 Layout and Style

If you are really interested in the rules of ho to place spaces in the code
and how to use new lines to create a blocks of code, then this chapter is fo you,
my friend.

### Chapter 32 Self-documenting code

Comments, do we need them if code is self-explanining? Returning back to pseudocode
that helps define design and useing it for comments for our code. And don't forget -
the comment should answer question *Why?* not *How?*.

### Chapter 33 Personal character

So, what kind of characteristics is separating good programmers out of bad ones?
I did liked the subchapter about characteristics that don't matter as much as
many people think - persistence, experience and gonzo programming. Can't agree more.

### Checklist

The big part of the book is a checklist in the end of each chapter with questions
that hopefully help programmer to refrech important topics and check his code or
design process.

### Quotes

And at last motivating (or not) quotes that I think pretty good even in the current
time.

> The architecture should explain why a single database is preferable to multiple databases (or vice versa), explain why a database is preferable to flat files, identify possible interactions with other programs that access the same data, explain what views have been created on the data, and so on

> The most radical solution to building software is not to build it at all — to buy it instead or to download open-source software for free

> If necessary, plan the architecture work as a separate project, too

> Design Is About Tradeoffs and Priorities. If minimizing development time is more important, a good designer will craft a different design

> Designing the class interface is an iterative process just like any other aspect of design. If you don’t get the interface right the first time, try a few more times until it stabilizes. If it doesn’t stabilize, you need to try a different approach

> When you come up with a first design attempt that seems good enough, don’t stop!

> A final risk of prototyping arises when developers do not treat the code as throwaway code

> A small number of objects might cause performance issues, but programmers are notoriously poor at guessing which code really causes problems

> Fail hard during development so that you can fail softer during production

> Once you’ve written the pseudocode and designed the data, take a minute to review the pseudocode you’ve written. Back away from it, and think about how you would explain it to someone else.

> People are more willing to review a few lines of pseudocode than they are to review 35 lines of C++ or Java.

> Once you start coding, you get emotionally involved with your code and it becomes harder to throw away a bad design and start over

> The greater the flexibility desired, the higher the complexity of the code needed to support that flexibility and the more error-prone the code will be. Because successful programming depends on minimizing complexity, a skilled programmer will build in as much flexibility as needed to meet the software’s requirements but will not add flexibility — and related complexity — beyond what’s required

> It’s OK to figure out murder mysteries, but you shouldn’t need to figure out code. You should be able to read it

> Complicated code is a sign that you don’t understand your program well enough to make it simple

> You must hope to find errors in your code. Such a hope might seem like an unnatural act, but you should hope that it’s you who finds the errors and not someone else

> Most errors tend to be concentrated in a few highly defective routines

> If you’re programming by trial and error, defects are guaranteed. You don’t need to learn how to fix defects; you need to learn how to avoid them in the first place

> Programmers treat small changes casually. They don’t desk-check them, they don’t have others review them, and they sometimes don’t even run the code to verify that the fix works properly

> Sometimes the cheapest and best way to improve a program’s performance is to buy new hardware

> Jackson’s Rules of Optimization: Rule 1. Don’t do it. Rule 2 (for experts only). Don’t do it yet — that is, not until you have a perfectly clear and unoptimized solution

> Programmers are notorious for saying that a program is “90 percent complete” during the last 50 percent of the project

## Chapter 3 Measure Twice, Cut Once: Upstream Prerequisites

### 3.1 Importance of Prerequisites

#### Do Prerequisites Apply to Modern Software Projects?

By far the most common project risks in software development are poor requirements
and poor project planning, thus preparation tends to focus on improving requirements
and project plans.

#### Causes of Incomplete Preparation

Studies over the last 25 years have proven conclusively that it pays to do things right
the first time. **Unnecessary changes are expensive.**

### 3.3 Problem-Definition Prerequisite

The first prerequisite you need to fulfill before beginning construction is a clear
statement of the problem that the system is supposed to solve. This is sometimes called
“product vision”, “vision statement”, “mission statement” or “product definition.”
Here it’s called “problem definition”.

### 3.4 Requirements Prerequisit

#### Why Have Official Requirements?

Explicit requirements keep you from guessing what the user wants.
Explicit requirements also help to avoid arguments.

#### Handling Requirements Changes During Construction

If you’re driving from Chicago to Los Angeles, is it a waste of
time to stop and look at a road map when you see signs for New York? No. If you’re
not heading in the right direction, stop and check your course.

### 3.5 Architecture Prerequisite

#### Program Organization

In the architecture, you should find evidence that alternatives to the final organization were considered and find the reasons for choosing the final organization over its alternatives.
It’s frustrating to work on a class when it seems as if the class’s role in the system
has not been clearly conceived.

Each building block is a class, or it’s a collection of classes or routines that work together on high-level functions such as interacting with the user, displaying Web pages, interpreting commands, encapsulating business rules, or accessing data.
Every feature listed in the requirements should be covered by at least one building block.

What each building block is responsible for should be well defined. A building block
should have one area of responsibility, and it should know as little as possible about
other building blocks’ areas of responsibility. By minimizing what each building block
knows about the other building blocks, you localize information about the design into
single building blocks.

#### Major Classes

Aim for the 80/20 rule: specify the 20 percent of the classes that make up 80 percent of the system’s behavior (Jacobsen, Booch, and Rumbaugh 1999; Kruchten 2000).

#### Data Design

> The architecture should explain why a single database is preferable to multiple databases (or vice versa), explain why a database is preferable to flat files,
identify possible interactions with other programs that access the same data, explain
what views have been created on the data, and so on.

#### Overengineering

Specifying an approach to overengineering is particularly important because **many
programmers overengineer their classes automatically, out of a sense of professional
pride**. By setting expectations explicitly in the architecture, you can avoid the phenomenon in which some classes are exceptionally robust and others are barely adequate.

#### Buy-vs.-Build Decisions

> The most radical solution to building software is not to build it at all — to buy it instead or to download open-source software for free. 

### 3.6 Amount of Time to Spend on Upstream Prerequisites

Generally, a well-run project devotes about 10 to 20 percent of its effort
and about 20 to 30 percent of its schedule to requirements, architecture,
and up-front planning (McConnell 1998, Kruchten 2000).

>  If necessary, plan the architecture work as a separate project, too.

#### Key points

- The overarching **goal of preparing for construction is risk reduction**. Be sure your preparation activities are reducing risks, not increasing them
- If you want to develop high-quality software, attention to quality must be part of the software-development process from the beginning to the end. **Attention to quality at the beginning** has a greater influence on product quality than attention at the end
- Part of a programmer’s job is to educate bosses and coworkers about the software-development process, including the importance of adequate preparation before programming begins
- The kind of project you’re working on significantly affects construction prerequisites
- Many projects should be highly iterative, and some should be more sequential
- If a good problem definition hasn’t been specified, **you might be solving the wrong problem** during construction
- If good requirements work hasn’t been done, you might have missed important details of the problem. **Requirements changes cost 20 to 100 times** as much in the stages following construction as they do earlier, so be sure the requirements are right before you start programming
- If a good architectural design hasn’t been done, **you might be solving the right problem the wrong way** during construction. The cost of architectural changes increases as more code is written for the wrong architecture, so be sure the architecture is right, too
- Understand what approach has been taken to the construction prerequisites on your project, and choose your construction approach accordingly
  
## Chapter 4 Key Construction Decisions

### 4.4 Selection of Major Construction Practice

Some projects use pair programming and test-first development,
while others use solo development and formal inspections. Either combination
of techniques can work well, depending on specific circumstances of the project.

### Key Points

- More construction practices exist than you can use on any single project. Consciously choose the practices that are best suited to your project.
- Ask yourself whether the programming practices you’re using are a response to the programming language you’re using or controlled by it. Remember to program into the language, rather than programming in it.
- Your position on the technology wave determines what approaches will be effective - or even possible. Identify where you are on the technology wave, and adjust your plans and expectations accordingly

## Chapter 5 Design in Construction

> “Design” might be just writing a class interface in pseudocode before writing the details.
It might be drawing diagrams of a few class relationships before coding them.
It might be asking another programmer which design pattern seems like a better choice.

### 5.1 Design Challenges

#### Design Is a Wicked Problem

Horst Rittel and Melvin Webber defined a “wicked” problem as one that could be
clearly defined only by solving it, or by solving part of it (1973). This paradox implies,
essentially, that **you have to “solve” the problem once in order to clearly define it and
then solve it again to create a solution that works**.

#### Design Is a Sloppy Process (Even If it Produces a Tidy Result)

Design is sloppy because you take many false steps and go down many blind alleys - 
you make a lot of mistakes. Indeed, making mistakes is the point of design - it’s
cheaper to make mistakes and correct designs than it would be to make the same mistakes,
recognize them after coding, and have to correct full-blown code.

Design is also sloppy because it’s hard to know **when your design is "good enough"**.
How much detail is enough? How much design should be done with a formal design
notation, and how much should be left to be done at the keyboard? When are you
done? Since design is open-ended, the most common answer to that question is
**"When you’re out of time"**.

#### Design Is About Tradeoffs and Priorities

> If minimizing development time is more important, a good designer will craft a different design.

#### Design Involves Restrictions

The point of design is partly to create possibilities and partly to **restrict possibilities**.

#### Design Is a Heuristic Process

Because design is nondeterministic, design techniques tend to be heuristics - **“rules of thumb”** or **“things to try that sometimes work”** - rather than repeatable processes that are guaranteed to produce predictable results. **Design involves trial and error**.

### 5.2 Key Design Concepts

#### Software’s Primary Technical Imperative: Managing Complexity

##### Importance of Managing Complexity

> Managing complexity is the most important technical topic in software development.
In my view, it’s so important that Software’s Primary Technical Imperative has to be
_managing complexity_.

One symptom that you have bogged down in complexity overload is when you find yourself doggedly applying a method that is clearly irrelevant, at least to any outside observer. It is like the mechanically inept person whose car breaks down - so he puts water in the battery and empties the ashtrays.

Dijkstra pointed out that **no one’s skull is really big enough to contain a modern computer program**
(Dijkstra 1972), which means that we as software developers shouldn’t try to cram whole programs
into our skulls at once; **we should try to organize our programs in such a way that we can safely
focus on one part of it at a time**.
The goal is to minimize the amount of a program you have to think about at any one time.
The goal of all software-design techniques is to break a complicated problem into simple pieces.

##### How to Attack Complexity

Ineffective designs arise from three sources:

 - A complex solution to a simple problem
 - A simple, incorrect solution to a complex problem
 - An inappropriate, complex solution to a complex problem
 
A two-prong approach to managing complexity:

- Minimize the amount of essential complexity that anyone’s brain has to deal with at any one time
- Keep accidental complexity from needlessly proliferating

#### Desirable Characteristics of a Design

> When I am working on a problem I never think about beauty.
I think only how to solve the problem. But when I have finished,
if the solution is not beautiful, I know it is wrong.
>
> R. Buckminster Fuller

List of internal design characteristics:

- **Minimal complexity** The primary goal of design should be to minimize complexity
  for all the reasons just described. **Avoid making “clever” designs**.
- **Ease of maintenance** This means designing for the maintenance
  programmer. _Continually imagine the questions a maintenance programmer would
  ask about the code you’re writing_.
- **Loose coupling** This means designing so that you hold connections
  among different parts of a program to a minimum.
  Minimal connectedness minimizes work during integration, testing, and maintenance.
- **Extensibility** This means that you can change a piece of a system without
  affecting other pieces.
- **Portability** This means designing the system so that you can easily move it to
  another environment.
- **Leanness** This means designing the system so that it has no extra parts. _Extra code has to be developed, reviewed, tested, and considered when the other code is modified_. Fatal question: “It’s easy, so what will we hurt by putting it in?” :(
- **Stratification** Design the system so that you can view it at one level
  without dipping into other levels.

#### Levels of Design

##### Level 1: Software System

Some programmers jump right from the system
level into designing classes, but it’s usually beneficial to think through higher level
combinations of classes, such as subsystems or packages.

##### Level 2: Division into Subsystems or Packages

The major design activity at this level is deciding how to partition the program
into major subsystems and defining how each subsystem is allowed to use each other subsystem. 

If all subsystems can communicate with all other subsystems,
you lose the benefit of separating them at all.
Make each subsystem meaningful by restricting communications.

If every subsystem ends up communicating directly with every other subsystem, 
this raises some important questions:

- How many different parts of the system does a developer need to understand at least a little bit to change something in the graphics subsystem?
- What happens when you try to use the business rules in another system?
- What happens when you want to put a new user interface on the system, perhaps a command-line UI for test purposes?

You want to architect your system so that if you pull out a subsystem to use elsewhere,
you won’t have many hoses to reconnect and those hoses will reconnect easily.

Common subsystems:

- Business rules
- User Interface
- Database access
- System dependencies

##### Level 3 Division into Classes

##### Level 4 Division into Routines

##### Level 5 Internal Routine Design

### 5.3 Design Building Blocks: Heuristics

#### Find Real-World Objects

1. Determine what can be done to each object
1. Determine what each object is allowed to do to other objects
1. Determine the parts of each object that will be visible to other objects
1. Define each object’s interfaces

#### Encapsulate Implementation Details

- **Abstraction** says, “You’re allowed to look at an object at a high level of detail”
- **Encapsulation** says, “Furthermore, you aren’t allowed to look at an object at any other level of detail”

#### Hide Secrets (Information Hiding)

Designing the class interface is an iterative process just like any other aspect of design. If you don’t get the interface right the first time, try a few more times until it stabilizes. If it doesn’t stabilize, you need to try a different approach.

Get into the habit of asking “What should I hide?”. You’ll be surprised at how many difficult design issues dissolve before your eyes.

#### Identify Areas Likely to Change

The goal is to isolate unstable areas so that the effect of a change will be limited to one routine,
class, or package.

1. Identify items that seem likely to change
1. Separate items that are likely to change
1. Isolate items that seem likely to change

Here are a few areas that are likely to change:

- Business rules
- Hardware dependencies
- Input and Output
- Difficult design and construction areas (They might be done poorly, thus need to change)
- Status variables
    - **Don't use boolean variable as status variable**, use an enumerated type instead
  
#### Anticipating Different Degrees of Change

A good technique for identifying areas likely to change is first to identify the minimal
subset of the program that might be of use to the user. The subset makes up the core
of the system and is unlikely to change.

By identifying the core first, you can see which components are really add-ons and
then extrapolate and hide improvements from there.

#### Keep Coupling Loose

Model railroad cars are coupled by opposing hooks that latch when pushed together. Connecting two cars is easy — you just push the cars together. The coupling of model railroad cars works because it’s as simple as possible. In software, make the connections among modules as simple as possible.

##### Coupling Criteria

- **Size** Number of connections between modules
- **Visibility** Passing data in a parameter list is making an obvious connection and is therefore good.
- **Flexibility** how easily you can change the connections between modules.

The more easily other modules can call a module, the more loosely coupled it is,
and that’s good because it’s more flexible and maintainable. In creating a system
structure, break up the program along the lines of minimal interconnectedness.

##### Kinds of Coupling

- **Simple-data-parameter coupling** if all the data passed between them are of primitive data types
  and all the data is passed through parameter lists
- **Simple-object coupling** A module is simple-object coupled to an object
  if it instantiates that object
- **Object-parameter coupling** Two modules are object-parameter coupled to each
  other if Object1 requires Object2 to pass it an Object3
- **Semantic coupling** _The most insidious kind of coupling occurs when one module
  makes use not of some syntactic element of another module but of some semantic
  knowledge of another module’s inner workings_
  
Semantic coupling is dangerous because changing code in the used module can break
code in the using module in ways that are completely undetectable by the compiler.

**Classes and routines are first and foremost intellectual tools for reducing complexity**. If they’re not making your job simpler, they’re not doing their jobs.

#### Look for Common Design Patterns

One potential trap with patterns is **force-fitting code to use a pattern**.
In some cases, shifting code slightly to conform to a well-recognized pattern
will improve understandability of the code. But if the code has to be shifted too far,
forcing it to look like a standard pattern can sometimes increase complexity.

#### Other Heuristics

##### Aim for Strong Cohesion

Cohesion refers to how closely all the routines in a class or all the code in
a routine support a central purpose — how focused the class is. Cohesion is a useful tool
for managing complexity because the more that code in a class supports a central purpose, the
more easily your brain can remember everything the code does.

##### Build Hierarchies
##### Formalize Class Contracts
##### Assign Responsibilities
##### Design for Test
##### Avoid Failure
##### Make Central Points of Control
##### Consider Using Brute Force
##### Draw a Diagram
##### Keep Your Design Modular

#### Guidelines for Using Heuristics

> One of the most effective guidelines is not to get stuck on a single approach.
If diagramming the design in UML isn’t working, write it in English. Write a short test program. Try a completely different approach. Think of a brute-force solution.
Keep outlining and sketching with your pencil, and your brain will follow. If all else fails, walk away from the problem. Literally go for a walk, or think about something else before returning to the problem. 

Some people are uncomfortable if they don’t come to closure after a design cycle, but after you have created a few designs without resolving issues prematurely, it will seem natural to leave issues unresolved until you have more information (Zahniser 1992, Beck 2000).

### 5.4 Design Practices

#### Iterate

You might have had an experience in which you learned so much from writing a program that you wished you could write it again, armed with the insights you gained
from writing it the first time. Design is an iterative process. You don’t usually go from point A only to point B; you
go from point A to point B and back to point A.

Switching from one view of a system to another is mentally strenuous, but it’s essential to creating effective designs. **When you come up with a first design attempt that seems good enough, don’t stop!** The second attempt is nearly always better than the first, and you learn things on each attempt that can improve your overall design.

#### Divide and Conquer

Incremental refinement is a powerful tool for managing complexity.
As Polya recommended in mathematical problem solving, understand the problem, devise a plan,
carry out the plan, and then look back to see how you did (Polya 1957).

#### Top-Down and Bottom-Up Design Approaches

Top-down design begins at a high level of abstraction.
You define base classes or other nonspecific design elements.
As you develop the design, you increase the level of detail, identifying derived
classes, collaborating classes, and other detailed design elements.

Bottom-up design starts with specifics and works toward generalities. It typically
begins by identifying concrete objects and then generalizes aggregations of objects
and base classes from those specifics.

##### Argument for Top Down

Continue decomposing until it seems as if it would **be easier to code the next level**
than to decompose it.

#### Experimental Prototyping

> A final risk of prototyping arises when developers do not treat the code as throwaway
code.

#### Collaborative Design

#### How Much Design is Enough?

The biggest design errors arise from cases in which I thought I went far enough,
but it later turns out that I didn’t go far enough to realize there were additional
design challenges. In other words, the biggest design
problems tend to arise not from areas I knew were difficult and created bad designs
for, **but from areas I thought were easy** and didn’t create any designs for at all.

I would rather see 80 percent of the design
effort go into creating and exploring numerous design alternatives and 20 percent go
into creating less polished documentation than to have 20 percent go into creating
mediocre design alternatives and 80 percent go into polishing documentation of
designs that are not very good.

#### Capturing Your Design Work

- **Insert design documentation into the code itself** it improves the chance that programmers will keep the design documentation reasonably up to date
- Capture design discussions and desicions on a Wiki
- Write e-mail summaries
- **Use a digital camera** Taking pictures of whiteboard drawings with a digital camera
  and then embedding those pictures into traditional documents can be a low-effort way
  to get 80 percent of the benefit of saving design drawings by doing about 1 percent of the work required if you use a drawing tool.
- **Use CRC (Class, Responsibility, Collaborator) cards** Another low-tech alternative for documenting designs is to use index cards. On each card, designers write a class name, responsibilities of the class, and collaborators (other classes that cooperate with the class).
- Create UML disagrams at **appropriate** levels of detail

## Chapter 6 Working Classes

### 6.1 Class Foundations: Abstract Data Types (ADTs)

Without understanding ADTs, programmers create classes that are “classes” in name
only - in reality, they are little more than convenient carrying cases for loosely related
collections of data and routines.

### 6.2 Goog Class Interfaces

#### Good Abstraction

##### Be sure you understand what abstraction the class is implementing

The programmer should have exposed just the 15 grid-control routines plus
a 16th routine that supported cell coloring. By exposing all 150 routines,
the programmer created the possibility that, if we ever wanted to change
the underlying implementation, we could find ourselves supporting 150 public routines.

##### Provide services in pairs with their opposites

Most operations have corresponding, equal, and opposite operations.
If you have an operation that turns a light on, you’ll probably need one to turn it off.
**Don’t create an opposite gratuitously, but do check to see whether you need one**.

##### Move unrelated information to another class

In some cases, you’ll find that half a class’s routines work with half the class’s data
and half the routines work with the other half of the data. In such a case,
you really have two classes masquerading as one. **Break them up**!

##### Make interfaces programmatic rather than semantic when possible

##### Beware of erosion of the interface’s abstraction under modification

As a class is modified and extended, you often discover additional functionality that’s needed,
that doesn’t quite fit with the original class interface, but that seems too hard to implement
any other way.

##### Don’t add public members that are inconsistent with the interface abstraction 

##### Consider abstraction and cohesion together

##### Minimize accessibility of classes and members

##### Don’t expose member data in public

##### Avoid putting private implementation details into a class’s interface

##### Don’t make assumptions about the class’s users 

##### Avoid friend classes 

##### Don’t put a routine into the public interface just because it uses only public routines

##### Favor read-time convenience to write-time convenience 

Code is read far more times than it’s written, even during initial development.

##### Be very, very wary of semantic violations of encapsulation

Here are some examples of the ways that a user of a class can break encapsulation semantically:

- Not calling Class A’s InitializeOperations() routine because you know that Class
  A’s PerformFirstOperation() routine calls it automatically.
- **Not calling the database.Connect() routine before you call employee.Retrieve(
  database ) because you know that the employee.Retrieve() function will connect
  to the database if there isn’t already a connection**
- Not calling Class A’s Terminate() routine because you know that
  Class A’s PerformFinalOperation() routine has already called it.
- Using Class B’s MAXIMUM_ELEMENTS constant instead of using
  ClassA.MAXIMUM_ELEMENTS, because you know that they’re both equal to
  the same value.
  
> Anytime you find yourself looking at a class’s implementation to figure out how to use the class, you’re not programming to the interface; you’re programming through the interface to the implementation.

##### Watch for coupling that’s too tight

### 6.3 Design and Implementation Issues

#### Containment (“has a” Relationships)

#### Inheritance (“is a” Relationships)

##### Implement “is a” through public inheritance

If the derived class isn’t going to adhere completely to the same interface contract
defined by the base class, inheritance is not the right implementation technique.

##### Be suspicious of classes of which there is only one instance

A single instance might indicate that the design confuses objects with classes.
Consider whether you could just create an object instead of a new class.
Can the variation of the derived class be represented in data rather than as a distinct class?
The Singleton pattern is one notable exception to this guideline.

##### Be suspicious of base classes of which there is only one derived class

When I see a base class that has only one derived class, I suspect that **some programmer has been “designing ahead”** — trying to anticipate future needs, usually without fully understanding what those future needs are. The best way to prepare for future work is not to design extra layers of base classes that “might be needed someday”; it’s to make current work as clear, straightforward, and simple as possible.
That means not creating any more inheritance structure than is absolutely necessary

##### Be suspicious of classes that override a routine and do nothing inside the derived routine

The place to fix this problem is not in the base class, but in the original Cat class. Create a Claws class and contain that within the Cats class. The root problem was the
assumption that all cats scratch, so fix that problem at the source, rather than just
bandaging it at the destination.

##### Avoid deep inheritance trees

Arthur Riel suggests limiting inheritance hierarchies to a maximum of six levels.
Riel bases his recommendation on the “magic number 7±2,” but I think that’s grossly optimistic.
In my experience most people have trouble juggling more than two or three levels of inheritance in their brains at once.

##### Make all data private, not protected

#### Multiple Inheritance

Mixins are called mixins because they allow properties to be “mixed in” to derived classes.
Mixins require the use of multiple inheritance, but they aren’t subject to the classic
diamond-inheritance problem associated with multiple inheritance
as long as all mixins are truly independent of each other.

#### Why Are There So Many Rules for Inheritance?

For the sake of controlling complexity, you should maintain a heavy bias against inheritance.
Here’s a summary of when to use inheritance and when to use containment:

- If multiple classes share common data but not behavior, create a common object
  that those classes can contain.
- If multiple classes share common behavior but not data, derive them from a
  common base class that defines the common routines.
- If multiple classes share common data and behavior, inherit from a common
  base class that defines the common data and routines.
- Inherit when you want the base class to control your interface; contain when
  you want to control your interface.
  
#### Member Functions and Data

- Keep the number of routines in a class as small as possible
- Disallow implicitly generated member functions and operators you don’t want
- Minimize the number of different routines called by a class
- **Minimize indirect routine calls to other classes** Direct connections are hazardous
  enough. Indirect connections - such as `account.ContactPerson().DaytimeContactInfo().PhoneNumber()` even more so
- In general, **minimize the extent to which a class collaborates with other classes**

#### Constructors

- **Initialize all member data in all constructors, if possible**  Initializing all data members in all constructors is an inexpensive defensive programming practice.
- Prefer deep copies to shallow copies until proven otherwise

>  A small number of objects might cause performance issues, but programmers are notoriously poor at guessing which code really causes problems.

### 6.4 Reasons to Create a Class

1. Model real-world objects
1. **Model abstract objects** Circle and Square really exist,
    but Shape is an abstraction of other specific shapes
1. **Reduce complexity**
1. Isolate complexity
1. Hide implementation details 
1. Limit effects of changes 
1. Hide global data 
1. Streamline parameter passing
1. Make central points of control
1. **Facilitate reusable code** Even if a section of code is called from only one place in the program and is understandable as part of a larger class, it makes sense to put it into its own class if that piece of code might be used in another program.
    > Notably, the core of NASA’s approach to creating reusable classes does not involve “designing for reuse.” NASA identifies reuse candidates at the ends of their projects. They then perform the work needed to make the classes reusable as a special project at the end of the main project or as the first step in a new project. This approach helps prevent “gold-plating”—creation of functionality that isn’t required and that unnecessarily adds complexity.
1. **Plan for a family of programs** Thinking through not just what one program will look like but what the whole family of programs might look like is a powerful heuristic for anticipating entire categories of changes (Parnas 1976).
1. Package related operations
1. Accomplish a specific refactoring

#### Classes to Avoid

- Avoid creating god classes
- Eliminate irrelevant classes
- Avoid classes named after verbs (A class that has only behavior but no data is generally not really a class)
    
## Chapter 7 High-Quality Routines

Routine smell:

-  The routine’s input variable, is changed. If it’s an input variable, its value should not be modified
- The routine reads and writes global variables
- The routine doesn’t have a single purpose
- The routine doesn’t defend itself against bad data
- The routine uses several magic numbers
- Some of the routine’s parameters are unused
- The routine has too many parameters. The upper limit for an understandable number of parameters is about 7

### 7.1 Valid Reasons to Create a Routine

1. **Reduce complexity**  The single most important reason to create a routine is to reduce a program’s complexity. But after it’s written, you should be able to forget the details and use the routine without any knowledge of its internal workings. One indication that a routine needs to be broken out of another routine is deep nesting of an inner loop or a conditional.
1. **Introduce an intermediate, understandable abstraction** Putting a section of code into a well-named routine is one of the best ways to document its purpose.
1. Avoid duplicate code
1. **Support subclassing** You need less new code to override in a short, well-factored routine than a long, poorly factored routine.
1. Improve portability
1. **Simplify complicated boolean tests**
1. Improve performance
1. _To ensure all routines are small?_ **No**. With so many good reasons for putting code into a routine, this one is unnecessary.
    
#### Operations That Seem Too Simple to Put Into Routines

Constructing a whole routine to contain two or three lines of code might seem like overkill, but experience shows how helpful a good small routine can be. This example hints at another reason to put small operations into functions: **small operations tend to turn into larger operations**.

### 7.2 Design at the Routine Level

For routines, cohesion refers to how closely the operations in a routine are related. Some programmers prefer the term “strength”: how strongly related are the operations in a routine? 

Several kinds of cohesion are normally considered to be less than ideal:

- **Sequential cohesion** exists when a routine contains operations that must be performed in a specific order, that share data from step to step, and that don’t make up a complete function when done together
- **Communicational cohesion** occurs when operations in a routine make use of the same data and aren’t related in any other way. If a routine prints a summary report and then reinitializes the summary data passed into it, the routine has communicational cohesion: the two operations are related only by the fact that they use the same data
- **Temporal cohesion** occurs when operations are combined into a routine because they are all done at the same time
- **Procedural cohesion** occurs when operations in a routine are done in a specified order
- **Logical cohesion** occurs when several operations are stuffed into the same routine and one of the operations is selected by a control flag that’s passed in
- **Coincidental cohesion** occurs when the operations in a routine have no discernible relationship to each other

### 7.3 Good Routine Names

- **Describe everything the routine does**
- **Avoid meaningless, vague, or wishy-washy verbs**
- **Make names of routines as long as necessary** Routine names are often attached to object names,
    which essentially provides part of the name for free.
- **To name a function, use a description of the return value**
- **To name a procedure, use a strong verb followed by an object**
- **Use opposites precisely** Opposite-pairs like first/last are commonly understood
- **Establish conventions for common operations**

### 7.5 How to Use Routine Parameter

- If several routines use similar parameters, put the similar parameters in a consistent order
- Use all the parameters
- Don’t use routine parameters as working variables
- Put status or error variables last
- Document interface assumptions about parameters. If you assume the data being passed to your routine has certain characteristics, document the assumptions as you make them. Even better than commenting your assumptions, use assertions to put them into code
- Limit the number of a routine’s parameters to about seven. If you are passing the same data to many different routines, group the routines into a class and treat the frequently used data as class data
- Pass the variables or objects that the routine needs to maintain its interface abstraction. There are two competing schools of thought about how to pass members of an object to a routine.

    - Proponents of the first school of thought argue that **only the three specific elements needed by the routine should be passed**. They argue that doing this will keep the connections between routines to a minimum; reduce coupling; and make them easier to understand, reuse, and so on. They say that passing the whole object to a routine violates the principle of encapsulation by potentially exposing all 10 access routines to the routine that’s called.
    - Proponents of the second school argue that **the whole object should be passed**. They argue that the interface can remain more stable if the called routine has the flexibility to use additional members of the object without changing the routine’s interface. They argue that passing three specific elements violates encapsulation by exposing which specific data elements the routine is using.
        
    > If you find yourself frequently changing the parameter list to the routine, with the parameters coming from the same object each time, that’s an indication that you
    should be passing the whole object rather than specific elements.
    
### 7.6 Special Considerations in the Use of Functions

> A function is a routine that returns a value; a procedure is a routine that does not.

#### When to Use a Function and When to Use a Procedure

The function would always be named for the value it returned, as sin(), CustomerID(), and ScreenHeight() are. A procedure, on the other hand, could take input, modify, and output parameters — as many of each as it wanted to.

A common programming practice is to have a function that operates as a procedure and
returns a status value. The alternative is to create a procedure that has a status variable as an explicit parameter.

## Chapter 8 Defensive Programming

> In defensive driving, you adopt the mindset that you’re never sure
what the other drivers are going to do.

### 8.2 Assertions

- That an input parameter’s value falls within its expected range (or an output
    parameter’s value does)
- **That the value of an input-only variable is not changed by a routine**
- That an array or other container passed into a routine can contain at least X number of data elements
- That a container is empty (or full) when a routine begins executing (or when it finishes)
- That the results from a highly optimized, complicated routine match the results from a slower but clearly written routine

During production, they can be compiled out of the code so that the assertions don’t degrade system performance.

#### Guidelines for Using Assertions

> Use error-handling code for conditions you expect to occur; use assertions for
conditions that should never occur

For highly robust code, assert and then handle the error anyway.

### 8.3 Error-Handling Techniques

- **Return a neutral value** A drawing routine that displays x-ray data for cancer patients, however, would not want to display a “neutral value.” In that case, you’d be better off shutting down the program than displaying incorrect patient data.
- **Substitute the next piece of valid data** If you’re taking readings from a thermometer 100 times per second and you don’t get a valid reading one time, you might simply wait another 1/100th of a second and take the next reading.
- **Return the same answer as the previous time**
- **Substitute the closest legal value**
- **Log a warning message to a file**
- **Return an error code**
- **Call an error-processing routine/object**
- **Display an error message wherever the error is encountered** Attackers sometimes use error messages to discover how to attack a system
- **Handle the error in whatever way works best locally**
- **Shut down**

#### Robustness vs. Correctness

**Correctness** means never returning an inaccurate result;
returning no result is better than returning an inaccurate result.

**Robustness** means always trying to do something that will allow the software to keep operating,
even if that leads to results that are inaccurate sometimes.

### 8.4 Exceptions

> Don’t throw an uncaught exception in a section of code if you can handle the error locally

You should always consider the full set of error-handling alternatives: handling the error locally, propagating the error by using an error code, logging debug information to a file, shutting down the system, or using some other approach.

Sometimes the best response to a serious run-time error is to release all acquired resources and abort. Let the user rerun the program with proper input.

### 8.5 Barricade Your Program to Contain the Damage Caused by Errors

> The class’s public methods assume the data is unsafe, and they are responsible for checking the data and sanitizing it.
Once the data has been accepted by the class’s public methods, the class’s private
methods can assume the data is safe.

The easiest way to do this is usually by sanitizing external data as it arrives,
but data often needs to be sanitized at more than one level,
so multiple levels of sterilization are sometimes required.

#### Relationship Between Barricades and Assertions

**Routines that are outside the barricade** should use **error handling** because it
isn’t safe to make any assumptions about the data. **Routines inside the barricade**
should use **assertions**, because the data passed to them is supposed to be sanitized
before it’s passed across the barricade.

### 8.6 Debugging Aids

#### Don’t Automatically Apply Production Constraints to the Development Version

Be willing to trade speed and resource usage during development in exchange for
built-in tools that can make development go more smoothly.

#### Introduce Debugging Aids Early

Typically, you won’t go to the effort of writing a debugging aid until after you’ve been bitten by a problem several times.

#### Use Offensive Programming

Suppose you have a case statement that you expect to handle only five kinds of
events. During development, the default case should be used to generate a warning
that says “Hey! There’s another case here! Fix the program!” During production,
however, the default case should do something more graceful,
like writing a message to an error-log file.

Here are some ways you can program offensively:

- [ ] Make sure asserts abort the program. Don’t allow programmers to get into the
    habit of just hitting the Enter key to bypass a known problem.
    Make the problem painful enough that it will be fixed
- [ ] Be sure the code in each case statement’s default or else clause fails hard (aborts the program) or is otherwise impossible to overlook
- [ ] Fill an object with junk data just before it’s deleted
- [ ] Set up the program to e-mail error log files to yourself so that you can see the kinds of errors that are occurring in the released software, if that’s appropriate for the kind of software you’re developing

Sometimes the best defense is a good offense.

> Fail hard during development so that you can fail softer during production.

### 8.8 Being Defensive About Defensive Programming

Too much defensive programming creates problems of its own. If you check data
passed as parameters in every conceivable way in every conceivable place,
your program will be fat and slow. What’s worse, the additional code needed for defensive programming
adds complexity to the software. Code installed for defensive
programming is not immune to defects, and you’re just as likely to find a defect in
defensive-programming code as in any other code - more likely, if you write the code
casually.

## Chapter 9 The Pseudocode Programming Process

### 9.1 Summary of Steps in Building Classes and Routines

#### Steps in Creating a Class

- Create a general design for the class
    1. Define the class’s specific responsibilities
    1. Define what “secrets” the class will hide
    1. Define exactly what abstraction the class interface will capture
    1. Determine whether the class will be derived from another class and whether other classes will be allowed to derive from it
    1. Identify the class’s key public methods
    1. Identify and design any nontrivial data members used by the class
- Construct each routine within the class
- Review and test the class as a whole

### 9.2 Pseudocode for Pros

Here are guidelines for using pseudocode effectively:

- Use English-like statements that precisely describe specific operations
- **Avoid syntactic elements from the target programming language**.
    Pseudocode allows you to design at a slightly higher level than the code itself.
    When you use programming-language constructs, you sink to a lower level, eliminating the main benefit of design at a higher level, and you saddle yourself with unnecessary syntactic restrictions.
- Write pseudocode at the level of intent. Describe the meaning of the approach rather than how the approach will be implemented in the target language.
- Write pseudocode at a low enough level that generating code from it will be nearly automatic. If the pseudocode is at too high a level, it can gloss over problematic details in the code. Refine the pseudocode in more and more detail until it seems as if it would be easier to simply write the code.
    
> When the pseudocode statements are converted to comments, they’ll be a good
explanation of the code’s intent.

Here are the benefits you can expect from using this style of pseudocode:

- Pseudocode makes reviews easier. You can review detailed designs without examining source code
- Pseudocode supports the idea of iterative refinement
- Pseudocode makes changes easier. A few lines of pseudocode are easier to change
than a page of code
- Pseudocode minimizes commenting effort. In the PPP, the pseudocode statements become the comments, so it actually takes more work to remove the comments than to leave them in
- Pseudocode is easier to maintain than other forms of design documentation. As long as the inline comments are maintained, the pseudocode’s documentation of the design will be accurate
  
### 9.3 Constructing Routines by Using the PPP

#### Design the Routine

##### Check the prerequisites

##### Define the problem the routine will solve

- The information the routine will hide
- Inputs to the routine
- Outputs from the routine
- Preconditions that are guaranteed to be true before the routine is called
- Postconditions that the routine guarantees will be true before it passes control back to the caller

##### Name the routine

If you have trouble creating a good name, that usually indicates that the purpose
of the routine isn’t clear.

##### Decide how to test the routine

As you’re writing the routine, think about how you can test it.

##### Research functionality available in the standard libraries

The single biggest way to improve both the quality of your code and your productivity is **to reuse good code**.

##### Think about error handling 

##### Think about efficiency

Don’t waste time scraping for incremental improvements until you know they’re needed.

##### Research the algorithms and data types

##### Write the pseudocode

Start with the general and work toward something more specific. The most general
part of a routine is a header comment describing what the routine is supposed to do,
so first write a concise statement of the purpose of the routine. Writing the statement
will help you clarify your understanding of the routine. Trouble in writing the general
comment is a warning that you need to understand the routine’s role in the program
better. In general, if it’s hard to summarize the routine’s role, you should probably
assume that something is wrong. 

##### Think about the data

##### Check the pseudocode 

Once you’ve written the pseudocode and designed the data, take a minute to review the pseudocode you’ve written. Back away from it, and **think about how you would explain it to someone else**.

> People are also more willing to review a few lines of pseudocode than they are to review 35 lines of C++ or Java.

##### Try a few ideas in pseudocode, and keep the best (iterate) 

> Once you start coding, you get emotionally involved with your code and it becomes harder to throw away a bad design and start over.

If you’re not sure how to code something, keep working with the pseudocode until you are sure. Keep refining and decomposing the pseudocode until it seems like a waste of time to write it instead of the actual code.

#### Code the Routine

#### Check the Code

- **Mentally check the routine for errors** 
- **Compile the routine** After the first compile, you step up the pressure: “I’ll get it right with just one more compile.” **“Just One More Compile” syndrome**. The point of this book is to show how to rise above the cycle of hacking something together and running it to see if it works.
- Step through the code in the debugger (**Even before the bug**)
- **Test the code**
- **Remove errors from the routine** If you find that a routine is unusually buggy, start over. Don’t hack around it - rewrite it. Creating an entirely new design for a buggy routine pays off

#### Clean Up Leftovers

- **Check the routine’s interface** Make sure that all input and output data is accounted for and that all parameters are used
- **Check for general design quality** Make sure the routine does one thing and does  it well, that it’s loosely coupled to other routines, and that it’s designed defensively
- **Check the routine’s variables** Check for inaccurate variable names, unused objects, undeclared variables, improperly initialized objects, and so on
- **Check the routine’s statements and logic** Check for off-by-one errors, infinite loops, improper nesting, and resource leaks
- **Check the routine’s layout** Make sure you’ve used white space to clarify the logical structure of the routine, expressions, and parameter lists
- **Check the routine’s documentation** Make sure the pseudocode that was translated into comments is still accurate. Check for algorithm descriptions, for documentation on interface assumptions and nonobvious dependencies, for justification of unclear coding practices
- **Remove redundant comments**

## Chapter 10 General Issues in Using Variables

### 10.4 Scope

- Initialize variables used in a loop immediately before the loop rather than back at the beginning of the routine containing the loop
- Don’t assign a value to a variable until just before the value is used
- **Group related statements**
- Break groups of related statements into separate routines
- Begin with most restricted visibility, and expand the variable’s scope only if
    necessary. It is much more difficult to reduce the scope of a variable that has had a large scope than to expand the scope of a variable that has had a small scope.
    It’s harder to turn a protected data member into a private data member than vice versa.
    
### 10.6 Binding Time

>  The greater the flexibility desired, the higher the complexity of the code needed
to support that flexibility and the more error-prone the code will be.
Because successful programming depends on minimizing complexity, a skilled programmer will build in as much flexibility as needed to meet the software’s requirements but will not add flexibility — and related complexity — beyond what’s required.

## Chapter 11 The Power of Variable Names

### 11.1 Considerations in Choosing Good Names

#### The Most Important Naming Consideration

Programmers sometimes overlook using the ordinary words, which is often the easiest solution.

#### Problem Orientation

> A good mnemonic name generally speaks to the problem rather than the solution

A record of employee data could be called `inputRec` or `employeeData`.
inputRec is a computer term that refers to computing ideas - input and record.
`employeeData` refers to the problem domain rather than the computing universe.
Similarly, for a bit field indicating printer status, `bitFlag` is a more computerish name than `printerReady`. In an accounting application, `calcVal` is more computerish than `sum`.

#### Common Opposites in Variable Names

- begin/end
- first/last
- locked/unlocked
- min/max
- next/previous
- old/new
- opened/closed
- visible/invisible
- source/target
- source/destination
- up/down

### 11.2 Naming Specific Types of Data

#### Naming Status Variables

**Think of a better name than flag for status variables** It’s better to think of flags as status variables. A flag should never have flag in its name because that doesn’t give you any clue about what the flag does.

> When you find yourself “figuring out” a section of code, consider renaming the variables. It’s OK to figure out murder mysteries, but you shouldn’t need to figure out
code. You should be able to read it.

#### Naming Boolean Variables

Here are some particularly useful boolean variable names:

- done
- error
- found
- success or ok

Some programmers like to put `is` in front of their boolean names.

### 11.3 The Power of Naming Conventions

#### Why Have Conventions?

- By making one global decision rather than many local ones, you can concentrate on the more important characteristics of the code
- They help you transfer knowledge across projects
- **They help you learn code more quickly on a new project**
- Without naming conventions, you can easily call the same thing by two different names
- They emphasize relationships among related items

> The key is that any convention at all is often better than no convention.

#### When You Should Have a Naming Convention

- When multiple programmers are working on a project
- When you plan to turn a program over to another programmer for modifications and maintenance (**which is nearly always**)
- When your programs are reviewed by other programmers in your organization
- When your program is so large that you can’t hold the whole thing in your brain at once and must think about it in pieces
- When the program will be long-lived enough that you might put it aside for a few weeks or months before working on it again
- When you have a lot of unusual terms that are common on a project and want to have standard terms or abbreviations to use in coding
    
#### Guidelines for Language-Specific Conventions

##### C Conventions

- c and ch are character variables.
- i and j are integer indexes.
- n is a number of something.
- p is a pointer.
- s is a string.

### 11.5 Standardized Prefixes

#### User-Defined Type Abbreviations

UDTs are described with short codes that you create for a specific program and then
standardize on for use in that program. The codes are mnemonics such as `win` for window and `scr` for screen regions.

### 11.7 Kinds of Names to Avoid

- **Avoid misleading names or abbreviations**
- **Avoid names with similar meanings** If you can switch the names of two variables
    without hurting the program, you need to rename both variables. For example, `input` and `inputValue`, `recordNum` and `numRecords`, and `fileNumber` and `fileIndex`
- **Avoid variables with different meanings but similar names** Avoid names like
    `clientRecs` and `clientReps`
- **Avoid names that sound similar, such as wrap and rap**
- **Avoid numerals in names**
- **Avoid misspelled words in names**
- **Don’t differentiate variable names solely by capitalization**
- **Avoid multiple natural languages** `color` and `colour`
- **Avoid names containing hard-to-read characters** `ttl5`, `ttlS`, `tt1S`

## Chapter 12 Fundamental Data Types

### 12.1 Numbers in General

- Avoid "magic numbers"
- Anticipate divide-by-zero errors
- Avoid mixed-type comparisons 

### 12.2 Integers

- Check for integer division  (The easiest way to remedy this problem is to reorder the expression so that the divisions are done last)
- Check for integer overflow

### 12.4 Characters and Strings

- Avoid magic characters and strings
- Know how your language and environment support Unicode
- Decide on an internationalization/localization strategy early in the lifetime of a program

### 12.5 Boolean Variables

- Use boolean variables to document your program
    ```java
    finished = ( ( elementIndex < 0 ) || ( MAX_ELEMENTS < elementIndex ) );
    repeatedEntry = ( elementIndex == lastElementIndex );
    if ( finished || repeatedEntry ) {}
    ```
- Use boolean variables to simplify complicated tests

### 12.6 Enumerated Types

- Use enumerated types for readability
    ```c++
    intresult = RetrievePayrollData( data, true, false, false, true );

    intresult = RetrievePayrollData(
        data,
        EmploymentStatus_CurrentEmployee,
        PayrollType_Salaried,
        SavingsPlan_NoDeduction,
        MedicalCoverage_IncludeDependents
    ) 
    ```
- Use enumerated types for reliability. If you use an enumerated type,
    declaring a variable as Color, the compiler will allow the variable to be assigned
    only the values Color_Red, Color_Green, and Color_Blue.
- Use enumerated types as an alternative to boolean variables
- Define the first and last entries of an enumeration for use as loop limits
- Reserve the first entry in the enumerated type as invalid

## Chapter 13 Unusual Data Types

### 13.1 Structures

- Use structures to clarify data relationships
    ```
    name = inputName
    address = inputAddress
    phone = inputPhone
    title = inputTitle
    department = inputDepartment
    bonus = inputBonus
    ```
    and
    ```
    employee.name = inputName
    employee.address = inputAddress
    employee.phone = inputPhone

    supervisor.title = inputTitle
    supervisor.department = inputDepartment
    supervisor.bonus = inputBonus
    ```

## Chapter 14 Organizing Straight-Line Code

### 14.1 Statements That Must Be in a Specific Order

```
revenue.ComputeMonthly();
revenue.ComputeQuarterly();
revenue.ComputeAnnual();
```

In this example, the quarterly revenue calculation assumes that the monthly revenues
have already been calculated. Because the routine calls don’t have any parameters,
you might be able to guess that each of these routines accesses class data. But you can’t know for sure from reading this code.

Here are some simple guidelines for ordering statements:
- Organize code so that dependencies are obvious
- Name routines so that dependencies are obvious 
- Use routine parameters to make dependencies obvious
    ```
    InitializeExpenseData( expenseData )
    ComputeMarketingExpense( expenseData )
    ComputeSalesExpense( expenseData )
    ComputeTravelExpense( expenseData )
    ComputePersonnelExpense( expenseData )
    DisplayExpenseSummary( expenseData ) 
    ```
    Because all the routines use expenseData, you have a hint that they might be working on the same data and that the order of the statements might be important.
- Document unclear dependencies with comments
- Check for dependencies with assertions or error-handling code
     For example, in the class’s constructor, you might initialize a class member variable `isExpenseDataInitialized` to `false`. Then in `InitializeExpenseData()`, you can set `isExpenseDataInitialized` to `true`. Each function that depends on `expenseData` being initialized can then check whether `isExpenseDataInitialized` has been set to `true` before performing additional operations on expenseData.

### 14.2 Statements Whose Order Doesn’t Matter

>  The guiding principle is the Principle of Proximity: Keep related actions together.

#### Making Code Read from Top to Bottom

As a general principle, make the program read from top to bottom rather than jumping around.

## Chapter 15 Using Conditionals

### 15.1 if Statements

#### Plain if-then Statements

> Check for reversal of the if and else clauses

#### Chains of if-then-else Statements

- Put the most common cases first 
- Make sure that all cases are covered. Code a final else clause with an error message or assertion to catch cases you didn’t plan for.

## Chapter 16 Controlling Loops

### 16.2 Controlling the Loop

#### Entering the Loop

- Put initialization code directly before the loop. The same kind of error can occur when you move or copy the loop code into a different routine without moving or copying its initialization code.

### 16.2 Controlling the Loop

#### How Long Should a Loop Be?

- Make your loops short enough to view all at once. You’ll rarely write loops longer
    than 15 or 20 lines.
- **Move loop innards of long loops into routines** If the loop is well designed, the code on the inside of a loop can often be moved into one or more routines that are called from within the loop.
- Make long loops especially clear

### 16.3 Creating Loops Easily — From the Inside Out

>  Here’s the general process.
Start with one case. Code that case with literals. Then indent it, put a loop around it, and replace the literals with loop indexes or computed expressions. Put another loop around that, if necessary, and replace more literals. Continue the process as long as you have to. When you finish, add all the necessary initializations.

### Chapter 17 Unusual Control Structures

#### 17.2 Recursion

For most problems, it produces massively complicated solutions — in those
cases, simple iteration is usually more understandable.

> The typical examples are computing a factorial or computing a Fibonacci sequence. Recursion is a powerful tool, and it’s really dumb to use it in either of those cases.

Third, and most important, you should consider alternatives to recursion before using it.

## Chapter 18 Table-Driven Methods

A table-driven method is a scheme that allows you to look up information in a table
rather than using logic statements (if and case) to figure it out.

### 18.1 General Considerations in Using Table-Driven Methods

You put your program’s knowledge into its data rather than into its logic - in the table instead of in the if tests.

Data tends to be more flexible than logic.
Data is easy to change when a message format changes.
If you have to add a new kind of message, you can just add another element to the data table.

## Chapter 19 General Control Issues

### 19.1 Boolean Expressions

#### Making Complicated Expressions Simple

- Break complicated tests into partial tests with new boolean variables
- Move complicated expressions into boolean functions.
    Putting the test into a well-named function improves readability and makes
    it easier for you to see what your code is doing, and that’s a sufficient reason to do it.
- Use decision tables to replace complicated conditions

> Complicated code is a sign that you don’t understand your program
well enough to make it simple.

### 19.6 Control Structures and Complexity

One reason so much attention has been paid to control structures is that they are a big
contributor to overall program complexity. Poor use of control structures increases
complexity; good use decreases it.
One measure of “programming complexity” is the number of mental objects you have
to keep in mind simultaneously in order to understand a program.

#### General Guidelines for Reducing Complexity

Perhaps the most influential of the numeric techniques is
Tom McCabe’s, in which complexity is measured by counting the number of “decision
points” in a routine.

Moving part of a routine into another routine doesn’t reduce the overall complexity of
the program; **it just moves the decision points around**. But it reduces the amount of
complexity you have to deal with at any one time.

#### Other Kinds of Complexity

The McCabe measure of complexity isn’t the only sound measure, but it’s the measure
most discussed in computing literature and it’s especially helpful when you’re thinking about control flow. Other measures include the amount of data used, the number
of nesting levels in control constructs, the number of lines of code, the number of
lines between successive references to variables (“span”), the number of lines that a
variable is in use (“live time”), and the amount of input and output. Some researchers
have developed composite metrics based on combinations of these simpler ones.

## Chapter 20 The Software-Quality Landscape

### 20.1 Characteristics of Software Quality

**External characteristics** are characteristics that a user of the software product is aware of:

- Correctness
- Usability
- Efficiency
- Reliability
- Integrity
- Adaptability
- Accuracy
- Robustness

External characteristics of quality are the only kind of software characteristics that
users care about.

Programmers care about the **internal characteristics** of the software as well as the
external ones.

- Maintainability
- Flexibility
- Portability
- Reusability
- Readability
- Testability
- Understandability

The point is that some quality characteristics are emphasized to make life easier
for the user and some are emphasized to make life easier for the programmer.

The attempt to maximize certain characteristics inevitably conflicts with the attempt to maximize others.

### 20.2 Techniques for Improving Software Quality

- **Software-quality objectives**  One powerful technique for improving software quality is setting explicit quality objectives from among the external and internal characteristics. The power of setting explicit goals
- **Explicit quality-assurance activity** The organization must show programmers that quality is a priority
- **Testing strategy**
- **Software-engineering guidelines**
- **Informal technical reviews**
- **Formal technical reviews** Inspection, a peer review, a customer review, or an audit
- **External audits**

#### Development Process

##### Change-control procedures

One big obstacle to achieving software quality is uncontrolled changes.
Uncontrolled requirements changes can result in disruption to design and coding.
Uncontrolled changes in design can result in code that doesn’t agree with its requirements, inconsistencies in the code, or more time spent modifying code to meet the changing design than spent moving the project forward. 

##### Measurement of results

##### Prototyping

### 20.3 Relative Effectiveness of Quality Techniques

#### Percentage of Defects Detected

- Informal design reviews 35%
- Formal design inspections 55%
- Informal code reviews 25%
- Formal code inspections 60%
- Modeling or prototyping 65%
- Personal desk-checking of code 40%
- Unit test 30%
- New function (component) test 30%
- Integration test 35%
- Regression test 25%
- System test 40%
- Low-volume beta test (<10 sites) 35%
- High-volume beta test (>1,000 sites) 75%

The strong implication is that if project developers are striving for a higher defectdetection rate, they need to use a combination of techniques.
 
Boeing and other companies have reported that different people tend to find different defects.

Glenford Myers points out that human processes (inspections and walk-throughs, for
instance) tend to be better than computer-based testing at finding certain kinds of
errors and that the opposite is true for other kinds of errors (1979). This result was confirmed in a later study, which found that code reading detected more interface defects and functional testing detected more control defects (Basili, Selby, and Hutchens 1986)

This data can also be used to understand why programmers who begin working with a
disciplined defect-removal technique such as **Extreme Programming** experience higher
defect-removal levels than they have experienced previously. 

#### Cost of Finding Defects

Most studies have found that inspections are cheaper than testing.

#### Cost of Fixing Defects

The longer a defect remains in the system, the more expensive it becomes to remove. Even more important, some techniques, such as inspections, detect the symptoms and causes of defects in one step; others, such as testing, find symptoms but require additional work to diagnose and fix the root cause.

### 20.4 When to Do Quality Assurance

> The earlier an error is inserted into software, the more entangled it becomes in other parts of the software and the more expensive it becomes to remove.

A requirements error can result in extra architecture or in bad architectural decisions. The extra architecture results in extra code, test cases, and documentation. It’s a good idea to catch requirements and architecture errors before they affect later activities.

### 20.5 The General Principle of Software Quality

The best way to improve productivity and quality is to reduce the time spent reworking code, whether the rework arises from changes in requirements, changes in design, or debugging.

The single biggest activity on most projects is debugging and correcting code that
doesn’t work properly.

It’s not necessarily the case that writing software without defects takes more time
than writing software with defects.
    
## Chapter 21 Collaborative Construction

In one way or another, all collaborative construction techniques are attempts to formalize the process of showing your work to someone else for the purpose of flushing out errors.

### 21.1 Overview of Collaborative Development Practices

Studies at the Software Engineering Institute have found that developers insert an average of 1 to 3 defects per hour into their designs and 5 to 8 defects per hour into code (Humphrey 1997), so attacking these blind spots is a key to effective construction.

#### Collaborative Construction Complements Other Quality-Assurance Techniques

The primary purpose of collaborative construction is to improve software quality. As
noted in Chapter 20, “The Software-Quality Landscape,” software testing has limited
effectiveness when used alone — the average defect-detection rate is only about
30 percent for unit testing, 35 percent for integration testing, and 35 percent for low-volume beta testing.

As Karl Wiegers points out, “A human reviewer can spot unclear error messages, inadequate comments, hard-coded variable values, and repeated code patterns that should be consolidated. Testing won’t” (Wiegers 2002).

#### Collaborative Construction Provides Mentoring in Corporate Culture and Programming Expertise

Reviews create a venue for more experienced and less experienced programmers to
communicate about technical issues. 

#### Collective Ownership Applies to All Forms of Collaborative Construction

Some methodologies, such as **Extreme Programming**, recommend formally pairing
programmers and rotating their work assignments over time. At my company, we’ve
found that programmers don’t need to pair up formally to achieve good code coverage.

### 21.2 Pair Programming

When pair programming, one programmer types in code at the keyboard and the
other programmer watches for mistakes and thinks strategically about whether the
code is being written correctly and whether the right code is being written.
Pair programming was originally popularized by Extreme Programming (Beck 2000).

#### Keys to Success with Pair Programming

- **Support pair programming with coding standards** Pair programming will not be effective if the two people in the pair spend their time arguing about coding style.
- **Don’t let pair programming turn into watching**
- **Don’t force pair programming of the easy stuff**
- **Rotate pairs and work assignments regularly**
- Encourage pairs to match each other’s pace
- Don’t force people who don’t like each other to pair
- Avoid pairing all newbies
- Assign a team leader

#### Benefits of Pair Programming

- It **holds up better under stress** than solo development. Pairs encourage each
    other to keep code quality high even when there’s pressure to write quick and dirty code.
- It **improves code quality**. The readability and understandability of the code
    tends to rise to the level of the best programmer on the team.
- It **shortens schedules**. Pairs tend to write code faster and with fewer errors.
    The project team spends less time at the end of the project correcting defects.
- It produces all the other general benefits of collaborative construction,
    including disseminating corporate culture, **mentoring junior programmers**,
    and fostering collective ownership.
    
### 21.3 Formal Inspections

- Checklists focus the reviewers’ attention on areas that have been problems in the past
- The inspection focuses on **defect detection, not correction**
- Reviewers prepare for the inspection meeting beforehand and arrive with a list of the problems they’ve discovered
- Distinct roles are assigned to all participants
- The moderator of the inspection isn’t the author of the work product under inspection
- The moderator has received specific training in moderating inspections
- The inspection meeting is held only if all participants have adequately prepared
- Data is collected at each inspection and is fed into future inspections to improve them
- General management doesn’t attend the inspection meeting unless you’re inspecting a project plan or other management materials. Technical leaders might attend

#### Roles During an Inspection

- Moderator
- Author
- Reviewer
- Scribe?
- Management?

Overall, an inspection should have no fewer than three participants. It’s not possible
to have a separate moderator, author, and reviewer with fewer than three people, and
those roles shouldn’t be combined. Traditional advice is to limit an inspection to
about six people because, with any more, the group becomes too large to manage.

#### General Procedure for an Inspection

- Planning
- Overview
    The design or code should speak for itself; the overview shouldn’t speak for it.
- Preparation
    A reviewer might be asked to prepare for the inspection from the point of view
    of the maintenance programmer, the customer, or the designer.
- Inspection Meeting. Don’t discuss solutions during the meeting.
    The group should stay focused on identifying defects.
    Some inspection groups don’t even allow discussion about whether a defect is really a defect.
    They assume that if someone is confused enough to think it’s a defect,
    the design, code, or documentation needs to be clarified.
- Inspection Report
    If you collect data on the time spent and the number of errors found over time,
    you can respond to challenges about inspection’s efficacy with hard data.
- Rework
- Follow-Up

#### Fine-Tuning the Inspection

As you do inspections, you’ll notice that certain kinds of errors occur more frequently
than other kinds. Create a checklist that calls attention to those kinds of errors
so that reviewers will focus on them.

#### Introspection Summary

Inspection checklists encourage focused concentration.
The inspection process is systematic because of its standard checklists and standard roles.
It is also self-optimizing because it uses a formal feedback loop to improve the checklists and to monitor preparation and inspection rates.

### 21.4 Other Kinds of Collaborative Development Practices

#### Walk-Throughs

People can call virtually any kind of review a "walk-through".
A review is basically a meeting, and meetings are expensive.
If you’re going to incur the overhead of holding a meeting,
it’s worthwhile to structure the meeting as a formal inspection.

#### Code Reading

Two or more people read the code. Use at least two people to encourage competition
between the reviewers. If you use more than two, measure everyone’s contribution
so that you know how much the extra people contribute.

The difference between code reading on the one hand and inspections and walkthroughs
on the other is that code reading focuses more on individual review of the
code than on the meeting. The result is that each reviewer’s time is focused on finding
problems in the code. Less time is spent in meetings in which each person contributes
only part of the time and in which a substantial amount of the effort goes
into moderating group dynamics.

A study of 13 reviews at AT&T found that the importance of the review meeting itself
was overrated; 90 percent of the defects were found in preparation for the review
meeting, and only about 10 percent were found during the review itself.

#### Dog-and-Pony Shows

Dog-and-pony shows are reviews in which a software product is demonstrated to a customer.

## Chapter 22 Developer Testing

- **Unit testing** is the execution of a complete class, routine, or small program that
    has been written by a single programmer or team of programmers, which is
    tested in isolation from the more complete system.
- **Component testing** is the execution of a class, package, small program, or other
    program element that involves the work of multiple programmers or programming teams,
    which is tested in isolation from the more complete system.
- **Integration testing** is the combined execution of two or more classes, packages,
    components, or subsystems that have been created by multiple programmers or
    programming teams.
- **Regression testing** is the repetition of previously executed test cases for the purpose
    of finding defects in software that previously passed the same set of tests.
- **System testing** is the execution of the software in its final configuration, including
    integration with other software and hardware systems. It tests for security, performance,
    resource loss, timing problems, and other issues that can’t be tested
    at lower levels of integration.
    
### 22.1 Role of Developer Testing in Software Quality

Testing is a hard activity for most developers to swallow for several reasons:

- Testing’s goal runs counter to the goals of other development activities. The goal
    is to find errors. **A successful test is one that breaks the software**.
    The goal of every other development activity is to prevent errors and keep the software from
    breaking.
- **Testing can never completely prove the absence of errors**.
- Testing by itself does not improve software quality. **If you want to improve your software,
    don’t just test more; develop better**.
- Testing requires you to assume that you’ll find errors in your code.
    > You must hope to find errors in your code. Such a hope might seem like an
    unnatural act, but you should hope that it’s you who finds the errors and not someone else
    
### 22.2 Recommended Approach to Developer Testing

- Test for each relevant requirement to make sure that the requirements have been
implemented.
- Test for each relevant design concern to make sure that the design has been implemented.
- Use "basis testing" to add detailed test cases to those that test the requirements
and the design. **At a minimum, you should test every line of code**.
- Use a checklist of the kinds of errors you’ve made on the project to date or have
    made on previous projects.
    
#### Test First or Test Last?

Writing test cases before writing the code doesn’t take any more effort than writing test
cases after the code; it simply resequences the test-case-writing activity.

#### Limitations of Developer Testing

- **Developer tests tend to be “clean tests”** Developers tend to test for whether the code works (clean tests) rather than test for all the ways the code breaks (dirty tests).
- Developer testing tends to have an optimistic view of test coverage
- Developer testing tends to skip more sophisticated kinds of test coverage. A better coverage
    standard is to meet what’s called “100% branch coverage,” with every predicate term being tested
    for at least one true and one false value.

### 22.3 Bag of Testing Tricks

#### Incomplete testing

When you’re planning tests, eliminate those that don’t tell you anything new — that is, tests on new data that probably won’t produce an error if other, similar data didn’t produce an error. 

#### Structured Basis Testing

The easiest way to make sure that you’ve gotten all the bases covered is to calculate the number of paths through the program and then develop the minimum number of test cases that will exercise every path through the program.

Since they cover all paths, they’re similar to structured basis testing, but they don’t include the idea of **covering all paths with a minimal set of test cases**. If you use code coverage or logic coverage testing, __you might create many more test cases than you would need to cover the same logic__ with structured basis testing.

Each keyword in the code represents something that can be either true or false; make sure you have at least one test case for each true and at least one for each false.

Boolean expressions without a lot of ands and ors have fewer variations to test. 

This kind of testing assures you only that all of the code will be executed. It does not account for variations in data.

#### Data-Flow Testing

Data-flow testing is based on the idea that **data usage is at least as error-prone as control flow**.

#### Equivalence Partitioning

A good test case covers a large part of the possible input data. If two test cases flush out exactly the same errors, you need only one of them. 

#### Error Guessing

The term “error guessing” is a lowbrow name for a sensible concept. It means creating test cases based upon guesses about where the program might have errors, although it implies a certain amount of sophistication in the guessing.

#### Boundary Analysis

The idea of boundary analysis is to write test cases that exercise the boundary conditions.

#### Classes of Bad Data

Typical bad-data test cases include:

- Too little data (or no data)
- Too much data
- The wrong kind of data (invalid data)
- The wrong size of data
- Uninitialized data

#### Classes of Good Data

When you try to find errors in a program, it’s easy to overlook the fact that **the nominal case might contain an error**. Usually the nominal cases described in the basis-testing section represent **one kind of good data**.

Checking each of these kinds of data can reveal errors, depending on the item being tested:
- Nominal cases—middle-of-the-road, expected values
- Minimum normal configuration
- Maximum normal configuration
- Compatibility with old data

An example of this would be saving a spreadsheet that’s as large as the “maximum spreadsheet size” advertised on the product’s packaging.

#### Use Test Cases That Make Hand-Checks Convenient

You might think that an ugly number like $90,783.82 would be more likely to reveal errors, but it’s no more likely to than any other number in its equivalence class.

### 22.4 Typical Errors

#### Which Classes Contain the Most Errors?

> Most errors tend to be concentrated in a few highly defective routines

They contained as many as 50 defects per 1000 lines of code, and fixing them often cost 10 times what it took to develop the whole system. (The costs included customer support and in-the-field maintenance.)

This is a clear illustration of the General Principle of Software Quality: improving quality improves the development schedule and reduces development costs.

#### Errors by Classification

- 25.18% Structural
- 22.44% Data
- 16.19% Functionality as implemented
- 9.88% Construction
- 8.98% Integration
- 8.12% Functional requirements
- 2.76% Test definition or execution
- 1.74% System, software architecture
- 4.71% Unspecified

#### Proportion of Errors Resulting from Faulty Construction

#### How Many Errors Should You Expect to Find?

The results of the TSP and cleanroom projects confirm another version of the General Principle of Software Quality: it’s cheaper to build high-quality software than it is to build and fix low-quality software.

#### Errors in Testing Itself

> Test cases are often as likely or more likely to contain errors than the code being tested (Weiland 1983, Jones 1986, Johnson 1994).

You can do several things to reduce the number of errors in your test cases:

- *Check your work* Step through test code in a debugger, line by line, just as you would production code
- *Plan test cases as you develop your software*
- *Keep your test cases*
- *Plug unit tests into a test framework*

### 22.5 Test-Support Tools

#### Building Scaffolding to Test Individual Classes

> A final kind of scaffolding is the dummy file, a small version of the real thing that has the same types of components that a full-size file has.

#### Diff Tools

#### Test-Data Generators

Here are some lessons from this story:

- Properly designed random-data generators can generate unusual combinations of test data that you wouldn’t think of.
- Random-data generators can exercise your program more thoroughly than you can.
- You can refine randomly generated test cases over time so that they emphasize a realistic range of input. This concentrates testing in the areas most likely to be exercised by users, maximizing reliability in those areas.
- Modular design pays off during testing. I was able to pull out the encryption and decryption code and use it independently of the user-interface code, making the job of writing a test driver straightforward.
- You can reuse a test driver if the code it tests ever has to be changed. Once I had corrected the two early errors, I was able to start retesting immediately.

#### Coverage Monitors

#### Data Recorder/Logging

#### Symbolic Debuggers

#### System Perturbers

#### Error Databases

> One powerful test tool is a database of errors that have been reported. 

### 22.6 Improving Your Testing

#### Planning to Test

One key to effective testing is planning from the beginning of the project to test. Putting testing on the same level of importance as design or coding means that time will be allocated to it, it will be viewed as important, and it will be a high-quality process.

#### Retesting (Regression Testing)

#### Automated Testing

Benefits of test automation include the following:

- **An automated test has a lower chance of being wrong than a manual test**
- Once you automate a test, it’s readily available for the rest of the project with little incremental effort on your part
- If tests are automated, they can be run frequently to see whether any code check-ins have broken the code. **Test automation is part of the foundation of test-intensive practices, such as the daily build and smoke test and Extreme Programming**
- Automated tests improve your chances of detecting any given problem at the earliest possible moment, which tends to minimize the work needed to diagnose and correct the problem.
- Automated tests provide a safety net for large-scale code changes because they increase your chance of quickly detecting defects inserted during the modifications.
- Automated tests are especially useful in new, volatile technology environments because they flush out changes in the environments sooner rather than later.

### 22.7 Keeping Test Records

Here are a few kinds of data you can collect to measure your project:

- Administrative description of the defect (the date reported, the person who reported it, a title or description, the build number, the date fixed)
- Full description of the problem
- Steps to take to repeat the problem
- Suggested workaround for the problem
- Related defects
- Severity of the problem — for example, fatal, bothersome, or cosmetic
- *Origin of the defect: requirements, design, coding, or testing*
- Subclassification of a coding defect: off-by-one, bad assignment, bad array index, bad routine call, and so on
- *Classes and routines changed by the fix*
- *Number of lines of code affected by the defect*
- *Hours to find the defect*
- *Hours to fix the defect*

Once you collect the data, you can crunch a few numbers to determine whether your project is getting sicker or healthier:

- Number of defects in each class, sorted from worst class to best, possibly nor-
malized by class size
- Number of defects in each routine, sorted from worst routine to best, possibly normalized by routine size
- *Average number of testing hours per defect found
- *Average number of defects found per test case
- *Average number of programming hours per defect fixed
- Percentage of code covered by test cases
- Number of outstanding defects in each severity classification

#### Personal Test Records

> In addition to project-level test records, you might find it useful to keep track of your personal test records. These records can include both a checklist of the errors you most commonly make as well as a record of the amount of time you spend writing code, testing code, and correcting errors.

## Chapter 23 Debugging

> Debugging is twice as hard as writing the code in the first place. Therefore, if you write the code as cleverly as possible, you are, by definition, not smart enough to debug it.
>
> — Brian W. Kernighan

On some projects, debugging occupies as much as 50 percent of the total development time. For many programmers, debugging is the hardest part of programming.

### 23.1 Overview of Debugging Issues

#### Role of Debugging in Software Quality

> The best way to build a quality product is to develop requirements carefully, design well, and use high-quality coding practices. **Debugging is a last resort**.

#### Variations in Debugging Performance

In addition to providing insight into debugging, the evidence supports the General Principle of Software Quality: improving quality reduces development costs. The best programmers found the most defects, found the defects most quickly, and made correct modifications most often. You don’t have to choose between quality, cost, and time — they all go hand in hand.

#### Defects as Opportunities

> If you’re programming by trial and error, defects are guaranteed. You don’t need to learn how to fix defects; you need to learn how to avoid them in the first place.

- Learn about the program you’re working on
- Learn about the kinds of mistakes you make
  > Once you find the mistake, ask yourself how and why you made it. How could you have found it more quickly?
- Learn about the quality of your code from the point of view of someone who has to read it
- Learn about how you solve problems
- Learn about how you fix defects

#### An Ineffective Approach

##### The Devil’s Guide to Debugging

- Find the defect by guessing. To find the defect, scatter print statements randomly throughout a program
- Don’t waste time trying to understand the problem
- Fix the error with the most obvious fix

##### Debugging by Superstition

> Even if an error at first appears not to be your fault, it’s strongly in your interest to assume that it is.

### 23.2 Finding a Defect

Debugging consists of finding the defect and fixing it. Finding the defect—and understanding it — is usually 90 percent of the work.

#### The Scientific Method of Debugging

1. Stabilize the error.
1. Locate the source of the error (the “fault”).
    * Gather the data that produces the defect.
    * Analyze the data that has been gathered, and form a hypothesis about the defect.
    * Determine how to prove or disprove the hypothesis, either by testing the program or by examining the code.
    * Prove or disprove the hypothesis by using the procedure identified in 2(c).
1. Fix the defect
1. Test the fix
1. **Look for similar errors**

##### Stabilize the Error

If a defect doesn’t occur reliably, it’s almost impossible to diagnose. Making an intermittent defect occur predictably is one of the most challenging tasks in debugging.

Stabilizing an error usually requires more than finding a test case that produces the error. It includes narrowing the test case to the simplest one that still produces the error. The goal of simplifying the test case is to make it so simple that changing any aspect of it changes the behavior of the error.

##### Locate the Source of the Error

#### Tips for Finding Defects

- Use all the data available to make your hypothesis
- Refine the test cases that produce the error
- Exercise the code in your unit test suite
- Use available tools
- **Reproduce the error several different ways**
- Generate more data to generate more hypotheses
- Use the results of negative tests
- Brainstorm for possible hypotheses
- **Keep a notepad by your desk, and make a list of things to try**
- Narrow the suspicious region of the code
- **Be suspicious of classes and routines that have had defects before**
- **Check code that’s changed recently**
- Expand the suspicious region of the code
- Integrate incrementally
- Check for common defects
- Talk to someone else about the problem. **Some people call this “confessional debug- ging.”**
- Take a break from the problem

##### Brute-Force Debugging

- Perform a full design and/or code review on the broken code.
- Throw away the section of code and redesign/recode it from scratch.
- Throw away the whole program and redesign/recode it from scratch.
- Compile code with full debugging information.
- Compile code at pickiest warning level and fix all the picky compiler warnings.
- Strap on a unit test harness and test the new code in isolation.
- Create an automated test suite and run it all night.
- Step through a big loop in the debugger manually until you get to the error condition.
- Instrument the code with print, display, or other logging statements.
- Compile the code with a different compiler.
- Compile and run the program in a different environment.
- Link or run the code against special libraries or execution environments that produce warnings when code is used incorrectly.
- Replicate the end-user’s full machine configuration.
- Integrate new code in small pieces, fully testing each piece as it’s integrated.

###### Set a maximum time for quick and dirty debugging

###### Make a list of brute-force techniques

Before you begin debugging a difficult error, ask yourself, “If I get stuck debugging this problem, is there some way that I am guaranteed to be able to fix the problem?”

#### Syntax Errors

### 23.3 Fixing a Defect

1. **Understand the problem before you fix it**. The best way to make your life difficult and corrode the quality of your program is to fix problems without really understanding them 
1. **Understand the program, not just the problem**. If you understand the context in which a problem occurs, you’re more likely to solve the problem completely rather than only one aspect of it
1. Confirm the defect diagnosis
1. Relax. Hurrying to solve a problem is one of the most time-ineffective things you can do. It leads to rushed judgments, incomplete defect diagnosis, and incomplete corrections
1. Save the original source code
1. **Fix the problem, not the symptom**
1. **Change the code only for good reason**
1. **Make one change at a time**
1. **Check your fix**
1. **Add a unit test that exposes the defect**
1. **Look for similar defects**

### 23.4 Psychological Considerations in Debugging

#### How “Psychological Set” Contributes to Debugging Blindness

Research has shown that the programmers who debug most effectively mentally slice away parts of the program that aren’t relevant during debugging (Basili, Selby, and Hutchens 1986).

#### How “Psychological Distance” Can Help

### 23.5 Debugging Tools—Obvious and Not-So-Obvious

#### Source-Code Comparators

#### Compiler Warning Messages

Set your compiler’s warning level to the highest, pickiest level possible, and fix the errors it reports.

#### Extended Syntax and Logic Checking

#### Execution Profilers

#### Test Frameworks/Scaffolding

#### Debuggers

## Chapter 24 Refactoring

Design follows requirements, and it is done carefully so that coding can proceed linearly, from start to finish, implying that most of the code can be written once, tested, and forgotten.

### 24.1 Kinds of Software Evolution

The key distinction between kinds of software evolution is whether the program’s quality improves or degrades under modification. 

**If you treat modifications as opportunities to tighten up the original design of the program, quality improves.**

A second distinction in the kinds of software evolution is the one between changes made during construction and those made during maintenance. These two kinds of evolution differ in several ways. **Construction changes** are usually made by the original developers.

#### Philosophy of Software Evolution

Evolution is at once hazardous and an opportunity to approach perfection. When you have to make a change, strive to improve the code so that future changes are easier.

### 24.2 Introduction to Refactoring

The key strategy in achieving The Cardinal Rule of Software Evolution is refactoring, which Martin Fowler defines as “a change made to the internal structure of the software to make it easier to understand and cheaper to modify without changing its observable behavior” (Fowler 1999). The word “refactoring” in modern programming grew out of Larry Constantine’s original use of the word **“factoring”** in structured programming, which referred to decomposing a program into its constituent parts as much as possible (Yourdon and Constantine 1979).

#### Reasons to Refactor

- **Code is duplicated**
- **A routine is too long**
- **A loop is too long or too deeply nested**
- **A class has poor cohesion**
- **A class interface does not provide a consistent level of abstraction**
- **A parameter list has too many parameters**
- Changes within a class tend to be compartmentalized. **You find yourself changing either one part of the class or another part of the class—but few changes affect both parts of the class.**
- **Changes require parallel modifications to multiple classes**
- **Inheritance hierarchies have to be modified in parallel**
- **Related data items that are used together are not organized into classes**
- **A routine uses more features of another class than of its own class**
- A primitive data type is overloaded
- A class doesn’t do very much
- A chain of routines passes **tramp data**
- **A middleman object isn’t doing anything**
- One class is overly intimate with another
- **A routine has a poor name**
- Data members are public. **They blur the line between interface and implementation**
- **A subclass uses only a small percentage of its parents’ routines**
- **Comments are used to explain difficult code**
- Global variables are used
- **A routine uses setup code before a routine call or takedown code after a routine call**
- **A program contains code that seems like it might be needed someday**
  - Requirements for the “design ahead” code haven’t been fully developed, which means the programmer will likely guess wrong about those future requirements. The “code ahead” work will ultimately be thrown away.
  - If the programmer’s guess about the future requirement is pretty close, the programmer still will not generally anticipate all the intricacies of the future requirement. These intricacies undermine the programmer’s basic design assumptions, which means the “design ahead” work will have to be thrown away.
  - Future programmers who use the “design ahead” code don’t know that it was “design ahead” code, or they assume the code works better than it does. **They assume that the code has been coded, tested, and reviewed to the same level as the other code**. They waste a lot of time building code that uses the “design ahead” code, only to discover ultimately that the “design ahead” code doesn’t actually work.
  - The additional “design ahead” code creates additional complexity, which calls for additional testing, additional defect correction, and so on. The overall effect is to slow down the project.

#### Reasons Not to Refactor

In common parlance, “refactoring” is used loosely to refer to fixing defects, adding functionality, modifying the design—essentially as a synonym for making any change to the code whatsoever. This common dilution of the term’s meaning is unfortunate. Change in itself is not a virtue, but purposeful change, applied with a teaspoonful of discipline, can be the key strategy that supports steady improvement in a program’s quality under maintenance and prevents the all-too-familiar software-entropy death spiral.

### 24.3 Specific Refactorings

#### Data-Level Refactorings

- Replace a magic number with a named constant
- Rename a variable with a clearer or more informative name
- Move an expression inline
- Replace an expression with a routine
- Introduce an intermediate variable
- Convert a multiuse variable to multiple single-use variables
- Use a local variable for local purposes rather than a parameter
- Convert a data primitive to a class
- Convert a set of type codes to a class or an enumeration
- Convert a set of type codes to a class with subclasses
- Change an array to an object
- Encapsulate a collection
- Replace a traditional record with a data class

#### Statement-Level Refactorings

- Decompose a boolean expression
- Move a complex boolean expression into a well-named boolean function
- Consolidate fragments that are duplicated within different parts of a conditional
- Use break or return instead of a loop control variable
- Return as soon as you know the answer instead of assigning a return value within nested if-then-else statements
- Replace conditionals (especially repeated case statements) with polymorphism
- Create and use null objects instead of testing for null values

#### Routine-Level Refactorings

- Extract routine/extract method
- Move a routine’s code inline
- Convert a long routine to a class
- Substitute a simple algorithm for a complex algorithm
- Add a parameter
- Remove a parameter
- Separate query operations from modification operations
- Combine similar routines by parameterizing them
- Separate routines whose behavior depends on parameters passed in
- Pass a whole object rather than specific fields
- Pass specific fields rather than a whole object
- Encapsulate downcasting

#### Class Implementation Refactorings

- Change value objects to reference objects
- Change reference objects to value objects
- Replace virtual routines with data initialization
- Change member routine or data placement
  - Pull a routine up into its superclass.
  - Pull a field up into its superclass.
  - Pull a constructor body up into its superclass.
  - Push a routine down into its derived classes.
  - Push a field down into its derived classes.
  - Push a constructor body down into its derived classes.
- Extract specialized code into a subclass
- Combine similar code into a superclass

#### Class Interface Refactorings

- Move a routine to another class
- Convert one class to two
- Eliminate a class
- Hide a delegate
- Remove a middleman
- Replace inheritance with delegation
- Replace delegation with inheritance
- Introduce a foreign routine
- Introduce an extension class
- Encapsulate an exposed member variable 
- Remove Set() routines for fields that cannot be changed
- Hide routines that are not intended to be used outside the class
- Encapsulate unused routines
- Collapse a superclass and subclass if their implementations are very similar

#### System-Level Refactorings

- Create a definitive reference source for data you can’t control
- Change unidirectional class association to bidirectional class association
- Change bidirectional class association to unidirectional class association
- Provide a factory method rather than a simple constructor
- Replace error codes with exceptions or vice versa

### 24.4 Refactoring Safely

- Save the code you start with
- **Keep refactorings small**
- **Do refactorings one at a time**
- Make a list of steps you intend to take
- Make a parking lot. **a list of the changes that you’d like to make at some point but that don’t need to be made right now**
- Make frequent checkpoints
- Use your compiler warnings
- Retest
- Add test cases
- Review the changes

Programmers treat small changes casually. They don’t desk-check them, they don’t have others review them, and they sometimes don’t even run the code to verify that the fix works properly.
The moral is simple: treat simple changes as if they were complicated.

##### Adjust your approach depending on the risk level of the refactoring

A refactoring like “Replace a magic number with a named constant” is relatively risk-free. Refactorings that involve class or routine interface changes, database schema changes, or changes to boolean tests, among others, tend to be more risky. 

#### Bad Times to Refactor

##### Don’t use refactoring as a cover for code and fix

Programmers will sometimes say they’re refactoring, when all they’re really doing is tweaking the code, hoping to find a way to make it work. Refactoring refers to changes in working code that do not affect the program’s behavior.

##### Avoid refactoring instead of rewriting

Sometimes code doesn’t need small changes — it needs to be tossed out so that you can start over.

### 24.5 Refactoring Strategies

- Refactor when you add a routine. When you add a routine, check whether related routines are well organized
- Refactor when you add a class. Adding a class often brings issues with existing code to the fore
- Refactor when you fix a defect. **Use the understanding you gain from fixing a bug to improve other code that might be prone to similar defects.**
- Target error-prone modules. **Is there a section of code that you and everyone else on your team is afraid of?**
- **Target high-complexity modules**
- In a maintenance environment, improve the parts you touch. **when you do touch a section of code, be sure you leave it better than you found it.**
- Define an interface between clean code and ugly code, and then move code across the interface

## Chapter 25 Code-Tuning Strategies

### 25.1 Performance Overview

#### Quality Characteristics and Performance

> We assume that the better we make the code, the more our clients and customers will like our software.

Users are more interested in tangible program characteristics than they are in code quality.

Performance is only loosely related to code speed. To the extent that you work on your code’s speed, you’re not working on other quality characteristics. Be wary of **sacrificing other characteristics to make your code faster**. 

#### Performance and Code Tuning

Once you’ve chosen efficiency as a priority, whether its emphasis is on speed or on size, you should consider several options before choosing to improve either speed or size at the code level.

- Program requirements
- Program design
- Class and routine design
- Operating-system interactions
- Code compilation
- Hardware
- Code tuning

##### Program Requirements

Before you invest time solving a performance problem, make sure that you’re solving a problem that needs to be solved.

##### Program Design

If you know that a program’s size and speed are important, design the program’s architecture so that you can reasonably meet your size and speed goals.

- Setting individual resource goals makes the system’s ultimate performance predictable. If each feature meets its resource goals, the whole system will meet its goals. You can identify subsystems that have trouble meeting their goals early and target them for redesign or code tuning.
- The mere act of making goals explicit improves the likelihood that they’ll be achieved. Programmers work to objectives when they know what they are; **the more explicit the objectives, the easier they are to work to**.
- You can set goals that don’t achieve efficiency directly but promote efficiency in the long run. Efficiency is often best treated in the context of other issues. For example, achieving a high degree of modifiability can provide a better basis for meeting efficiency goals than explicitly setting an efficiency target. **With a highly modular, modifiable design, you can easily swap less-efficient components for more-efficient ones**.

##### Class and Routine Design

##### Operating-System Interactions

You might not be aware that the program is interacting with the operating system; sometimes your compiler generates system calls or your libraries invoke system calls you would never dream of.

##### Code Compilation

##### Hardware

> Sometimes the cheapest and best way to improve a program’s performance is to buy new hardware

##### Code Tuning

### 25.2 Introduction to Code Tuning

Code tuning is appealing for several reasons. One attraction is that it seems to defy the laws of nature. It’s incredibly satisfying to take a routine that executes in 20 microseconds, tweak a few lines, and reduce the execution speed to 2 microseconds.
It’s also appealing because mastering the art of writing efficient code is a rite of passage to becoming a serious programmer.

Nonetheless, within the programming culture, writing microefficient code proves you’re cool.

#### The Pareto Principle

> Complete it first, and then perfect it. The part that needs to be perfect is usually small.

#### Old Wives’ Tales

- Reducing the lines of code in a high-level language improves the speed or size of the resulting machine code — false!
- Certain operations are probably faster or smaller than others — false! You must always measure performance to know whether your changes helped or hurt your program. If you want your program to be portable, techniques that improve performance in one environment can degrade it in others.
- You should optimize as you go — false!
  - **It’s almost impossible to identify performance bottlenecks before a program is working completely**. Programmers are very bad at guessing which four percent of the code accounts for 50 percent of the execution time, and so programmers who optimize as they go will, on average, spend 96 percent of their time optimizing code that doesn’t need to be optimized.
  - In the rare case in which developers identify the bottlenecks correctly, they overkill the bottlenecks they’ve identified and allow others to become critical. Again, the ultimate effect is a reduction in performance. Optimizations done after a system is complete can identify each problem area and its relative importance so that optimization time is allocated effectively.
  - Focusing on optimization during initial development detracts from achieving other program objectives. **Developers immerse themselves in algorithm analysis and arcane debates that in the end don’t contribute much value to the user.** In short, **premature optimization’s primary drawback is its lack of perspective**.
- **A fast program is just as important as a correct one—false**!

#### When to Tune

> Jackson’s Rules of Optimization: Rule 1. Don’t do it. Rule 2 (for experts only). Don’t do it yet — that is, not until you have a perfectly clear and unoptimized solution.
>
> — M. A. Jackson

Use a high-quality design. Make the program right. Make it modular and easily modi- fiable so that it’s easy to work on later. When it’s complete and correct, check the performance. If the program lumbers, make it fast and small. Don’t optimize until you know you need to.

#### Compiler Optimizations

Optimizing compilers are better at optimizing straightforward code than they are at optimizing tricky code. If you do “clever” things like fooling around with loop indexes, your compiler has a harder time doing its job and your program suffers. Why not just write clear code and let the compiler do the work?

### 25.3 Kinds of Fat and Molasses

#### Common Sources of Inefficiency

- Input/output operations. **If you have a choice of working with a file in memory vs. on disk, in a database, or across a network, use an in-memory data structure unless space is critical.**
- Paging
- System calls. Calls to system routines are often expensive
- Interpreted languages
- Errors. A final source of performance problems is errors in the code. Errors can include leaving debugging code turned on (such as logging trace information to a file), forgetting to deallocate memory, improperly designing database tables, polling nonexistent devices until they time out, and so on

> Defining an index on a commonly used table is not optimization; it’s just good programming practice.

### 25.4 Measurement

> Many aspects of performance are counterintuitive. 

I learned that the only result of optimization you can usually be sure of without measuring performance is that you’ve made your code harder to read. 

#### Measurements Need to Be Precise

### 25.5 Iteration

### 25.6 Summary of the Approach to Code Tuning

1. Develop the software by using well-designed code that’s easy to understand and modify
1. If performance is poor,
    * Save a working version of the code so that you can get back to the “last
    known good state”
    * Measure the system to find hot spots
    * Determine whether the weak performance comes from inadequate design, data types, or algorithms and whether code tuning is appropriate. If code tuning isn’t appropriate, go back to step 1
    * Tune the bottleneck identified in step (c)
    * Measure each improvement one at a time
    * **If an improvement doesn’t improve the code, revert to the code saved in step (a).** (Typically, more than half the attempted tunings will produce only a negligible improvement in performance or degrade performance)
1. Repeat from step 2

## Chapter 26 Code-Tuning Techniques

The code-tuning changes described in this chapter might seem cosmetically similar to the refactorings described in Chapter 24, but **refactorings are changes that improve a program’s internal structure** (Fowler 1999). The changes in this chapter might better be called “anti-refactorings.” Far from “improving the internal structure,” **these changes degrade the internal structure in exchange for gains in performance**. If the changes didn’t degrade the internal structure, we wouldn’t consider them to be optimizations; we would use them by default and consider them to be standard coding practice.

### 26.1 Logic

#### Stop Testing When You Know the Answer

#### Order Tests by Frequency

Arrange tests so that the one that’s fastest and most likely to be true is performed first

#### Compare Performance of Similar Logic Structures

#### Substitute Table Lookups for Complicated Expressions

In some circumstances, a table lookup might be quicker than traversing a complicated chain of logic. The point of a complicated chain is usually to categorize something and then to take an action based on its category.

#### Use Lazy Evaluation

One of my former roommates was a great procrastinator. He justified his laziness by saying that many of the things people feel rushed to do simply don’t need to be done. If he waited long enough, he claimed, the things that weren’t important would be procrastinated into oblivion and he wouldn’t waste his time doing them.

### 26.2 Loops

#### Unswitching

#### Jamming

Jamming, or “fusion,” is the result of combining two loops that operate on the same set of elements. The gain lies in cutting the loop overhead from two loops to one.

#### Unrolling

The goal of loop unrolling is to reduce the amount of loop housekeeping.

#### Minimizing the Work Inside Loops

One key to writing effective loops is to minimize the work done inside a loop. If you can evaluate a statement or part of a statement outside a loop so that only the result is used inside the loop, do so. It’s good programming practice, and in some cases it improves readability.

#### Sentinel Values

#### Putting the Busiest Loop on the Inside

When you have nested loops, think about which loop you want on the outside and which you want on the inside.

#### Strength Reduction

### 26.3 Data Transformations

#### Use Integers Rather Than Floating-Point Numbers

Integer addition and multiplication tend to be faster than floating point. Changing a loop index from a floating point to an integer, for example, can save time.

#### Use the Fewest Array Dimensions Possible

#### Minimize Array References

A loop that repeatedly uses one element of an array is a good candidate for the application of this technique.

#### Use Supplementary Indexes

It’s often more efficient to keep track of the length of the structure rather than computing the length each time you need it.

#### Use Caching

As with other optimization techniques, caching adds complexity and tends to be error-prone.

### 26.4 Expressions

#### Exploit Algebraic Identities

Jon Bentley describes a program that tested whether sqrt(x) < sqrt(y) (1982). Since sqrt(x) is less than sqrt(y) only when x is less than y, you can replace the first test with x < y.

#### Use Strength Reduction

- Replace multiplication with addition
- Replace exponentiation with multiplication
- Replace trigonometric routines with their trigonometric identities
- Replace longlong integers with longs or ints (but watch for performance issues associated with using native-length vs. non-native-length integers)
- Replace floating-point numbers with fixed-point numbers or integers
- Replace double-precision floating points with single-precision numbers
- Replace integer multiplication-by-two and division-by-two with shift operations

#### Initialize at Compile Time

If you’re using a named constant or a magic number in a routine call and it’s the only argument, that’s a clue that you could precompute the number, put it into a constant, and avoid the routine call.

#### Be Wary of System Routines

#### Use the Correct Type of Constants

When a constant and its related variable are different types, the compiler has to do a type conversion to assign the constant to the variable.

#### Precompute Results

If the results are used many times, it’s often cheaper to compute them once and look them up the rest of the time.

At a more complicated level, you might compute a lookup table once when program execution begins, using it every time thereafter, or you might store results in a data file or embed them in a program.

Even without precomputing a table, you can precompute the complicated part of the expression outside the loop and use it inside the loop.

Optimizing a program by precomputation can take several forms:

- Computing results before the program executes, and wiring them into constants that are assigned at compile time
- Computing results before the program executes, and hard-coding them into variables used at run time
- Computing results before the program executes, and putting them into a file that’s loaded at run time
- Computing results once, at program startup, and then referencing them each time they’re needed
- Computing as much as possible before a loop begins, minimizing the work done inside the loop
- Computing results the first time they’re needed, and storing them so that you can retrieve them when they’re needed again

#### Eliminate Common Subexpressions

If you find an expression that’s repeated several times, assign it to a variable and refer to the variable rather than recomputing the expression in several places.

### 26.5 Routines

#### Rewrite Routines Inline

### 26.6 Recoding in a Low-Level Language

1. Write 100 percent of an application in a high-level language
1. Fully test the application, and verify that it’s correct
1. If performance improvements are needed after that, profile the application to identify hot spots. Since about 5 percent of a program usually accounts for about 50 percent of the running time, you can usually identify small pieces of the program as hot spots
1. Recode a few small pieces in a low-level language to improve overall performance

### 26.7 The More Things Change, the More They Stay the Same

According to the measurements in this chapter, the effect of any specific optimization is actually less predictable than it was 10 years ago. The effect of each code tuning is affected by the programming language, compiler, compiler version, code libraries, library versions, and compiler settings, among other things.
Code tuning invariably involves tradeoffs among complexity, readability, simplicity, and maintainability on the one hand and a desire to improve performance on the other.

## Chapter 27 How Program Size Affects Construction

If you’ve been accustomed to working on small projects, your first medium-to-large project can rage riotously out of control, becoming an uncontrollable beast instead of the pleasant success you had envisioned.

### 27.1 Communication and Size

The more communication paths you have, the more time you spend communicating and the more opportunities are created for communication mistakes. Larger-size projects demand organizational techniques that streamline communication or limit it in a sensible way.
The typical approach taken to streamlining communication is to formalize it in documents. Instead of having 50 people talk to each other in every conceivable combination, 50 people read and write documents.

### 27.2 Range of Project Sizes

### 27.3 Effect of Project Size on Errors

You might not think that error type would be affected, but as project size increases, a larger percentage of errors can usually be attributed to mistakes in requirements and design.

On small projects, construction errors make up about 75 percent of all the errors found. 

On larger projects, construction errors can taper off to about 50 percent of the total errors; requirements and architecture errors make up the difference.

You would naturally expect a project that’s twice as large as another to have twice as many errors. But the density of defects—the number of defects per 1000 lines of code—increases.

### 27.4 Effect of Project Size on Productivity

At small sizes (2000 lines of code or smaller), the single biggest influence on productivity is the skill of the individual programmer (Jones 1998). As project size increases, team size and organization become greater influences on productivity.

### 27.5 Effect of Project Size on Development Activities

#### Activity Proportions and Size

On a small project, construction is the most prominent activity by far, taking up as much as 65 percent of the total development time. 
On very large projects, architecture, integration, and system testing take up more time and construction becomes less dominant.

Proportions of activities vary because different activities become critical at different project sizes.

#### Programs, Products, Systems, and System Products

The simplest kind of software is a single “program” that’s used by itself by the person who developed it or, informally, by a few others.

A more sophisticated kind of program is a software “product,” a program that’s intended for use by people other than the original developer. A software product is used in environments that differ from the environment in which the product was created. It’s extensively tested before it’s released, it’s documented, and it’s capable of being maintained by others. A software product costs about three times as much to develop as a software program.

Another level of sophistication is required to develop a group of programs that work together. Such a group is called a software “system.” Development of a system is more complicated than development of a simple program because of the complexity of developing interfaces among the pieces and the care needed to integrate the pieces.

System products cost about nine times as much as simple programs

#### Methodology and Size

In social settings, the more formal the event, the more uncomfortable your clothes have to be (high heels, neckties, and so on). In software development, the more formal the project, the more paper you have to generate to make sure you’ve done your homework.

the more people’s brains you have to coordinate, the more formal documentation you need to coordinate them.

The point of your writing the plan is to force you to think carefully about configuration management and to explain your plan to everyone else. The documentation is a tangible side effect of the real work you do as you plan and construct a software system. If you feel as though you’re going through the motions and writing generic documents, something is wrong.

## Chapter 28 Managing Construction

### 28.1 Encouraging Good Coding

Sometimes a N project architect is just a senior person who has been around too long and is out of
touch with production coding issues. Programmers will resent that kind of “architect” defining standards that are out of touch with the work they’re doing.

#### Considerations in Setting Standards

Some developers welcome standards because they reduce arbitrary variance in the project.

#### Techniques for Encouraging Good Coding

##### Assign two people to every part of the project

If two people have to work on each line of code, you’ll guarantee that at least two people think it works and is readable.

##### Review every line of code

A code review typically involves the programmer and at least two reviewers. That means that at least three people read every line of code.

##### Require code sign-offs

In other fields, technical drawings are approved and signed by the managing engineer. The signature means that to the best of the engineer’s knowledge, the drawings are technically competent and error-free.

##### Route good code examples for review

One way to communicate your objectives is to circulate good code to your programmers or post it for public display.

In doing so, you provide **a clear example of the quality you’re aiming for**.

##### Emphasize that code listings are public assets

Extreme Programming’s idea of collective ownership

##### Reward good code

Use your organization’s reward system to reinforce good coding practices.

- The reward should be something that the programmer wants. (Many programmers find “attaboy” rewards distasteful, especially when they come from nontechnical managers.)
- Code that receives an award should be exceptionally good. If you give an award to a programmer everyone else knows does bad work, you look like Homer Simpson trying to run a nuclear reactor. It doesn’t matter that the programmer has a cooperative attitude or always comes to work on time. You lose credibility if your reward doesn’t match the technical merits of the situation. If you’re not technically skilled enough to make the good-code judgment, don’t! Don’t make the award at all, or let your team choose the recipient.

##### One easy standard

### 28.2 Configuration Management

#### What Is Configuration Management?

#### Requirements and Design Changes

During development, you’re bound to be bristling with ideas about how to improve the system. If you implement each change as it occurs to you, you’ll soon find yourself walking on a software treadmill—for all that the system will be changing, it won’t be moving closer to completion.

Here are some guidelines for controlling design changes:

- Follow a systematic change-control procedure
- Handle change requests in groups. It’s tempting to implement easy changes as ideas arise. write down all ideas and suggestions, no matter how easy they would be to implement, and save them until you have time to work on them. Then, viewing them as a group, choose the ones that will be the most beneficial.
- Estimate the cost of each change. Let all the interested parties know that software is intricately interwoven and that time estimation is necessary even if the change appears small at first glance.
- Be wary of high change volumes. a high volume of change requests is a key warning sign that requirements, architecture, or top-level designs weren’t done well enough to support effective construction.
- Establish a change-control board or its equivalent in a way that makes sense for your project. The board meets periodically to review proposed changes. It approves, disapproves, or defers each change. Change-control boards are considered a best practice for prioritizing and controlling requirements changes
- Watch for bureaucracy, but don’t let the fear of bureaucracy preclude effective change control

#### Software Code Changes

- Version-control software. Another style allows multiple people to work on files simultaneously and handles the issue of merging changes when the code is checked in. It becomes even more powerful when version control, defect tracking, and change management are integrated. 

#### Tool Versions

#### Machine Configurations

#### Backup Plan

### 28.3 Estimating a Construction Schedule

#### Estimation Approaches

- Use estimating software.
- Use an algorithmic approach, such as Cocomo II, Barry Boehm’s estimation model (Boehm et al. 2000).
- Have outside estimation experts estimate the project.
- Have a walk-through meeting for estimates.
- Estimate pieces of the project, and then add the pieces together.
- Have people estimate their own tasks, and then add the task estimates together.
- Refer to experience on previous projects.
- Keep previous estimates and see how accurate they were. Use them to adjust new estimates.

##### Establish objectives

Why do you need an estimate? What are you estimating? Are you estimating only construction activities, or all of development?

##### Allow time for the estimate, and plan it

Rushed estimates are inaccurate estimates. If you’re estimating a large project, treat estimation as a miniproject and take the time to miniplan the estimate so that you can do it well.

##### Spell out software requirements

Just as an architect can’t estimate how much a “pretty big” house will cost, you can’t reliably estimate a “pretty big” software project.
Define requirements or plan a preliminary exploration phase before making an estimate.

##### Estimate at a low level of detail

In general, the more detailed your examination is, the more accurate your estimate will be.

##### Use several different estimation techniques, and compare the results

##### Reestimate periodically

#### Estimating the Amount of Construction

#### Influences on Schedule

#### Estimation vs. Control

#### What to Do If You’re Behind

> The average project overruns its planned schedule by about 100 percent

##### Hope that you’ll catch up

One survey of over 300 software projects concluded that delays and overruns generally increase toward the end of a project (van Genuchten 1991). **Projects don’t make up lost time later; they fall further behind**.

##### Expand the team

**It’s like adding gas to a fire.** And merely increasing the number of people increases the complexity and amount of project communication.

Managers need to understand that developing software isn’t like riveting sheet metal: more workers working doesn’t necessarily mean more work will get done.

##### Reduce the scope of the project

If you eliminate a feature, you eliminate the design, coding, debugging, testing, and documentation of that feature. You eliminate that feature’s interface to other features.

Short of dropping a feature altogether, you can provide a cheaper version of the same functionality. 

Reestimate development time for the least important features. What functionality can you provide in two hours, two days, or two weeks?

### 28.4 Measurement

Make sure you’re collecting data for a reason. Set goals, determine the questions you need to ask to meet the goals, and then measure to answer the questions. Be sure that you ask for only as much information as is feasible to obtain, and keep in mind that **data collection will always take a back seat to deadlines**.

### 28.5 Treating Programmers as People

#### How Do Programmers Spend Their Time?

#### Variation in Performance and Quality

##### Individual Variation

##### Team Variation

> Good programmers tend to cluster, as do bad programmers

#### Religious Issues

Here’s a list of religious issues:
- Programming language
- Indentation style
- Placing of braces
- Choice of IDE
- Commenting style
- Efficiency vs. readability tradeoffs
- Choice of methodology—for example, Scrum vs. Extreme Programming vs. evolutionary delivery
- Programming utilities
- Naming conventions
- Use of gotos
- Use of global variables
- Measurements, especially productivity measures such as lines of code per day

If you think you need to control a programmer in any of these religious areas, consider these points:

- Be aware that you’re dealing with a sensitive area
- Use “suggestions” or “guidelines” with respect to the area
- Finesse the issues you can by sidestepping explicit mandates. **To finesse indentation style or brace placement, require source code to be run through a pretty-printer formatter before it’s declared finished. Let the pretty printer do the formatting**.
- Have your programmers develop their own standards

#### Physical Environment

### 28.6 Managing Your Manager

## Chapter 29 Integration

### 29.1 Importance of the Integration Approach

### 29.2 Integration Frequency—Phased or Incremental?

#### Phased Integration

When the classes are finally combined and errors surface by the score, programmers immediately go into panicky debugging mode rather than methodical error detection and correction.

#### Incremental Integration

1. Develop a small, functional part of the system. It can be the smallest functional part, the hardest part, a key part, or some combination. Thoroughly test and debug it. It will serve as a skeleton on which to hang the muscles, nerves, and skin that make up the remaining parts of the system.
1. Design, code, test, and debug a class.
1. Integrate the new class with the skeleton. Test and debug the combination of skeleton and new class. Make sure the combination works before you add any new classes. If work remains to be done, repeat the process starting at step 2.

#### Benefits of Incremental Integration

- Errors are easy to locate
- The system succeeds early in the project
- You get improved progress monitoring
- You’ll improve customer relations
- The units of the system are tested more fully
- You can build the system with a shorter development schedule

### 29.3 Incremental Integration Strategies

#### Top-Down Integration

In top-down integration, the class at the top of the hierarchy is written and integrated first. The top is the main window, the applications control loop, the object that contains main() in Java, WinMain() for Microsoft Windows programming, or similar.

#### Bottom-Up Integration

#### Sandwich Integration

You first integrate the high-level business-object classes at the top of the hierarchy. Then you integrate the device-interface classes and widely used utility classes at the bottom. These high-level and low-level classes are the bread of the sandwich.

#### Risk-Oriented Integration

Risk-oriented integration is also called “hard part first integration.” It’s like sandwich integration in that it seeks to avoid the problems inherent in pure top-down or pure bottom-up integration. Coincidentally, it also tends to integrate the classes at the top and the bottom first, saving the middle-level classes for last. The motivation, however, is different.
In risk-oriented integration, you identify the level of risk associated with each class. You decide which will be the most challenging parts to implement, and you implement them first. Experience indicates that top-level interfaces are risky, so they are often at the top of the risk list.

#### Feature-Oriented Integration

Another approach is to integrate one feature at a time. The term “feature” doesn’t refer to anything fancy, just an identifiable function of the system you’re integrating. You’ll usually want to start with a skeleton you’ve chosen for its ability to support the other features.

#### T-Shaped Integration

In this approach, one specific vertical slice is selected for early development and integration. That slice should exercise the system end-to-end and should be capable of flushing out any major problems in the system’s design assumptions. Once that vertical slice has been implemented—and any associated problems have been corrected—the overall breadth of the system can be developed.

### 29.4 Daily Build and Smoke Test

Whatever integration strategy you select, a good approach to integrating the software
is the **daily build and smoke test**.

Every file is compiled, linked, and combined into Elate an executable program every day, and the program is then put through a “smoke test,”
a relatively simple check to see whether the product “smokes” when it runs.

If the product worked on Day 17 and is broken on Day 18, something that happened between the two builds broke the product.

##### Build daily

The problem with this is that if the build is broken one week, you might go for several weeks before the next good build. When that happens, you lose virtually all of the benefit of frequent builds.

##### Check for broken builds

##### Smoke test daily

##### Keep the smoke test current

##### Automate the daily build and smoke test

##### Establish a build group

##### Add revisions to the build only when it makes sense to do so...

##### ...but don’t wait too long to add a set of revisions

##### Require developers to smoke test their code before adding it to the system

Developers need to test their own code before they add it to the build. A developer can do this by creating a private build of the system on a personal machine, which the developer then tests individually.

##### Create a holding area for code that’s to be added to the build

Part of the success of the daily build process depends on knowing which builds are good and which are not.

##### Create a penalty for breaking the build

Make it clear from the beginning that keeping the build healthy is one of the project’s top priorities.

##### Release builds in the morning

Some groups have found that they prefer to build overnight, smoke test in the early morning, and release new builds in the morning rather than the afternoon.

##### Build and smoke test even under pressure

Under stress, developers lose some of their discipline. They feel pressure to take construction shortcuts that they would not take under less stressful circumstances. They review and test their own code less carefully than usual. The code tends toward a state of entropy more quickly than it does during less stressful times.

#### What Kinds of Projects Can Use the Daily Build Process?

#### Continuous Integration

Developers frequently get out of sync when they make larger-scale changes.

## Chapter 30 Programming Tools

Use of a leading-edge tool set—and familiarity with the tools used—can increase productivity by 50 percent or more (Jones 2000; Boehm et al. 2000).

### 30.1 Design Tools

In one sense, these design tools are just fancy drawing packages. Using a simple graphics package or pencil and paper, you can draw everything that the tool can draw.

### 30.5 Building Your Own Programming Tools

#### Project-Specific Tools

Most medium-sized and large projects need special tools unique to the project. For example, you might need tools to generate special kinds of test data, to verify the quality of data files, or to emulate hardware that isn’t yet available.

> Part of planning for a project should be thinking about the tools that might be needed and allocating time for building them

#### Scripts

## Chapter 31 Layout and Style

## Chapter 32 Self-Documenting Code

### 32.1 External Documentation

##### Unit development folders

A unit-development folder (UDF), or software-development folder (SDF), is an informal document that contains notes used by a developer during construction. A “unit” is loosely defined, usually to mean a class, although it could also mean a package or a component. The main purpose of a UDF is to provide a trail of design decisions that aren’t documented elsewhere.

##### Detailed-design document

### 32.2 Programming Style as Documentation

### 32.3 To Comment or Not to Comment

Comments are easier to write poorly than well, and commenting can be more damaging than helpful.

> Design routines in pseudocode, and then convert the pseudocode to comments and fill in the code between them.

### 32.4 Keys to Effective Comments

#### Kinds of Comments

- Repeat of the Code
- **Explanation of the Code** They are useful, but usually that’s only because the code is confusing
- Marker in the Code
- **Summary of the Code** Such comments are more valuable than comments that merely repeat the code because a reader can scan them more quickly than the code.
- **Description of the Code’s Intent** A six-month study conducted by IBM found that maintenance programmers “most often said that understanding the original programmer’s intent was the most difficult problem”
- **Commenting Efficiently**
    > The time you spend “commenting” is really time spent understanding the program better, which is time that needs to be spent regardless of whether you comment.
- Use the Pseudocode Programming Process to reduce commenting time
- **Integrate commenting into your development style** Commenting done later takes more time because you have to remember or figure out what the code is doing instead of just writing down what you’re already thinking about.
    > If your design is hard to code, simplify the design before you worry about comments or code.

#### Optimum Number of Comments

> focus on whether each comment is efficient

### 32.5 Commenting Techniques

#### Commenting Individual Lines

Here are two possible reasons a line of code would need a comment:

- The single line is complicated enough to need an explanation.
- The single line once had an error, and you want a record of the error.

Endline comments also tend to be cryptic. The right side of the line usually doesn’t offer much room, and the desire to keep the comment on one line means that the comment must be short. Work then goes into making the line as short as possible instead of as clear as possible.

#### Commenting Paragraphs of Code

Another way of thinking about commenting at the level of intent is to think about what you would name a routine that did the same thing as the code you want to comment

For the record, the code itself is always the first documentation you should check. 

> Focus paragraph comments on the why rather than the how

Comments that explain how something is done usually operate at the programming-language level rather than the **problem level**. It’s nearly impossible for a comment that focuses on how an operation is done to explain the **intent of the operation**, and comments that tell how are often redundant.

- Use comments to prepare the reader for what is to follow
- Avoid abbreviations
- Comment anything that gets around an error or an undocumented feature in a language or an environment
- Justify violations of good programming style. If you’ve had to violate good programming style, explain why

> Commenting tricky code is exactly the wrong approach to take.

One study found that areas of source code with large numbers of comments also tended to have the most defects and to consume the most development effort

> If you have to ask yourself “Is this tricky?” it is

This advice applies mainly to code you’re writing for the first time

#### Commenting Data Declarations

- Comment the units of numeric data. If a number represents length, indicate whether the length is expressed in inches, feet, meters, or kilometers. If it’s time, indicate whether it’s expressed in elapsed seconds since 1-1-1980, milliseconds since the start of the program, and so on.
- Comment the range of allowable numeric values
- Comment coded meanings
- Comment limitations on input data. Make sure that expected and unexpected values are documented
- **Stamp comments related to a variable with the variable’s name. That way, string searches for the variable name will find the comment as well as the variable**

#### Commenting Routines

Many textbooks urge you to pile up a stack of information at the top of every routine, regardless of its size or complexity.

- Keep comments close to the code they describe. **During maintenance, comments that are far from the code tend not to be maintained with the code**.
- Describe each routine in one or two sentences at the top of the routine. **If you can’t describe the routine in a short sentence or two, you probably need to think harder about what it’s supposed to do**.
- Document parameters where they are declared. That makes for more work and, unfortunately, in practice usually means that the global data doesn’t get documented.
- Take advantage of code documentation utilities such as Javadoc
- Differentiate between input and output data
- Document interface assumptions. **As you’re writing the routine and realize that you’re making an interface assumption, write it down immediately**.
- Comment on the routine’s limitations
- Document the routine’s global effects
- Document the source of algorithms that are used
- Use comments to mark parts of your program

#### Commenting Classes, Files, and Programs

- General Guidelines for Class Documentation
    - Describe the design approach to the class
    - Describe limitations, usage assumptions, and so on
    - Comment the class interface
    - Don’t document implementation details in the class interface. Consequently, class interface files should contain information needed to use the class but not information needed to implement or maintain the inner workings of the class.
- General Guidelines for File Documentation
    - Describe the purpose and contents of each file
    - Put your name, e-mail address, and phone number in the block comment
    - Include a version-control tag
    - Include legal notices in the block comment
    - Give the file a name related to its contents
- The Book Paradigm for Program Documentation. In the Book Paradigm, code and its documentation are organized into several components similar to the components of a book to help programmers get a high-level view of the program.

## Chapter 33 Personal Character

### 33.1 Isn’t Personal Character Off the Topic?

> We’ve all had projects in which we spent 80 percent of the time working on a small piece we found interesting and 20 percent of the time building the other 80 percent of the program.

If you want to be great, you’re responsible for making yourself great. It’s a matter of your personal character.

### 33.2 Intelligence and Humility

Empirically it’s been shown that humble programmers who compensate for their fallibilities write code that’s easier for themselves and others to understand and that has fewer errors.

### 33.3 Curiosity

Once you admit that your brain is too small to understand most programs and you realize that effective programming is a search for ways to offset that fact, you begin a careerlong search for ways to compensate.

- **Build your awareness of the development process** If you’re working in a competitive software market, half of what you now need to know to do your job will be out of date in three years. If you’re not learning, you’re turning into a dinosaur.
- **Experiment**
- **Read about problem solving** Problem solving is the core activity in building computer software
- **Analyze and plan before you act**
- **Learn about successful projects** One especially good way to learn about programming is to study the work of the great programmers
- **Read!**
- **Read other books and periodicals** Pat yourself on the back for reading this book
- **Affiliate with other professionals**
- **Make a commitment to professional development** Good programmers constantly look for ways to become better

### 33.4 Intellectual Honesty

Part of maturing as a programming professional is developing an uncompromising sense of intellectual honesty. Intellectual honesty commonly manifests itself in several ways:

- **Refusing to pretend you’re an expert when you’re not**
- Readily admitting your mistakes
- **Trying to understand a compiler warning rather than suppressing the message**
- Clearly understanding your program — not compiling it to see if it works
- Providing realistic status reports
- **Providing realistic schedule estimates** and holding your ground when management asks you to adjust them

> Programmers are notorious for saying that a program is “90 percent complete” during the last 50 percent of the project.

If a certain software capability is worth $250K to a company and you estimate it will cost $750K to develop, the company shouldn’t develop the software.

### 33.5 Communication and Cooperation

Programming is communicating with another programmer first and communicating with the computer second.

### 33.6 Creativity and Discipline

Some creative programmers view the discipline of standards and conventions as stifling to their creativity. The opposite is true. Establish conventions in noncritical areas so that you can focus your creative energies in the places that count.

### 33.7 Laziness

It manifests itself in the habit of compiling a class to see if it works so that you can avoid the exercise of checking the class with your mind.

The second kind of laziness is “enlightened laziness”. You’re still lazy, but you’re getting around the problem by spending the smallest possible amount of time on something that’s unpleasant.

The third is “long-term laziness.” It is undoubtedly the most productive kind of laziness (provided that you ultimately save time by having written the tool). In these contexts, a certain amount of laziness is beneficial.

When you step through the looking glass, you see the other side of the laziness picture. “Hustle” or “making an effort” doesn’t have the rosy glow it does in high-school physical education class. Hustle is extra, unnecessary effort. It shows that you’re eager but not that you’re getting your work done. **It’s easy to confuse motion with progress, busyness with being productive**. 

### 33.8 Characteristics That Don’t Matter As Much As You Might Think

#### Persistence

Most of the time, persistence in software development is pigheadedness — it has little value. Persistence when you’re stuck on a piece of new code is hardly ever a virtue. Try redesigning the class, try an alternative coding approach, or try coming back to it later.

In debugging, it can be mighty satisfying to track down the error that has been annoying you for four hours, but it’s often better to give up on the error after a certain amount of time with no progress — say 15 minutes. Let your subconscious chew on the problem for a while. Try to think of an alternative approach that would circumvent the problem altogether. Rewrite the troublesome section of code from scratch. Come back to it later when your mind is fresh. Fighting computer problems is no virtue. Avoiding them is better.

> It’s hard to know when to give up, but it’s essential that you ask.

If I don’t solve the problem using this approach within the next 30 minutes, I’ll take 10 minutes to brainstorm about different approaches and try the best one for the next hour.

#### Experience

In software development, even basic knowledge changes rapidly.

Older programmers tend to be viewed with suspicion not just because they might be out of touch with specific technology but because they might never have been exposed to basic programming concepts that became well known after they left school.

Older programmers sometimes feel they’ve already earned their stripes and resent having to prove themselves year after year.

#### Gonzo Programming

Those all-night programming stints make you feel like the greatest programmer in the world, but then you have to spend several weeks correcting the defects you installed during your blaze of glory.

### 33.9 Habits

When was the last time you seriously questioned your formatting style?

If you have to choose between making code fast and making it readable, and you make the same choice every time, you’re not really choosing — **you’re responding out of habit**.

After you’ve been programming a long time, it’s hard to suddenly start saying, “How do I make this loop faster?” or “How do I make this code more readable?” These are habits that good programmers develop early.

It’s easier to replace an old habit with a new one than it is to eliminate one altogether. In programming, try to develop new habits that work. Develop the habits of writing a class in pseudocode before coding it and carefully reading the code before compiling it, for instance.

> Your personal character directly affects your ability to write computer programs.

## Chapter 34 Themes in Software Craftsmanship

### 34.1 Conquer Complexity

- **Dividing a system** into subsystems at the architecture level so that your brain can focus on a smaller amount of the system at one time
- Carefully **defining class interfaces** so that you can ignore the internal workings of the class
- Preserving the abstraction represented by the class interface so that your brain doesn’t have to remember arbitrary details
- **Avoiding deep inheritance** hierarchies because they are intellectually demanding
- **Avoiding deep nesting of loops** and conditionals because they can be replaced by simpler control structures that burn up fewer gray cells.
- Carefully defining your approach to error handling rather than using an arbitrary proliferation of different error-handling techniques.
- **Not allowing classes to grow into monster** classes that amount to whole programs in themselves
- **Keeping routines short**
- Using clear, **self-explanatory variable names** so that your brain doesn’t have to waste cycles remembering details like “i stands for the account index, and j stands for the customer index, or was it the other way around?”
- Minimizing the number of parameters passed to a routine, or, more important, passing only the parameters needed to preserve the routine interface’s abstraction
- **Using conventions** to spare your brain the challenge of remembering arbitrary, accidental differences between different sections of code.

In summary, a primary goal of software design and construction is conquering complexity.

### 34.2 Pick Your Process

On a small project, the talents of the individual programmer are the biggest influence on the quality of the software.

The way in which people work together determines whether their abilities are added to each other or subtracted from each other.

If you don’t know what you’re building, you can’t very well create a superior design for it. 

If you rush to coding before the foundation is complete, it will be harder to make fundamental changes in the system’s architecture. 

Testing won’t make your program more usable, faster, smaller, more readable, or more extensible.

### 34.3 Write Programs for People First, Computers Second

Maintenance programmers spend 50 to 60 percent of their time trying to understand the code they have to maintain, and they appreciate the time you put into documenting it.

### 34.4 Program into Your Language, Not in It

Don’t limit your programming thinking only to the concepts that are supported automatically by your language.

You don’t need to use global data or gotos just because your language supports them.

### 34.5 Focus Your Attention with the Help of Conventions

Programmers on large projects sometimes go overboard with conventions. They establish so many standards and guidelines that remembering them becomes a fulltime job. But programmers on small projects tend to go “underboard,” not realizing the full benefits of intelligently conceived conventions. You should understand their real value and take advantage of them; you should use them to provide structure in areas in which structure is needed.

### 34.6 Program in Terms of the Problem Domain

One way of working at a high level of abstraction is to work in terms of the programming problem rather than the computer-science solution.

### 34.7 Watch for Falling Rocks

“Tricky code” is a code phrase for “bad code.” **If you think code is tricky, think about rewriting it so that it’s not**.

A class’s having more errors than average is a warning sign. A few error-prone classes tend to be the most expensive part of a program.