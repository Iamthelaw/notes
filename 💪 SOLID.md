# 💪 S.O.L.I.D

## Single Responsibility Principle (SRP)
> Принцип единственности ответственности. Классы и методы должн быть ответственнен за конкретный функционал и не пытаться сделать все сам и сразу.

Данный принцип вырастает из проблемы возникающей при множественных ответственностях класса, что каждый раз при изменении класса есть риск внесения багов, которые затронут другие зоны ответственности класса.

### Примеры
Плохой код
```python
class UserService:
    def validate(user):
        pass

    def make_payment(from_user, to_user):
        pass
```

Хороший код
```python
class ValidationUserService:
    def validate(user):
        pass

class BankingUserService:
    def make_payment(from_user, to_user):
        pass
```
У каждого класса теперь есть своя зона ответственности. Когда мы хотим изменить логику работы платежей мы меняем только класс ответственный за платежи.

## Open-Closed Principle (OCP)
> Объекты и сущности должны быть открыты для расширения и закрыты для изменения.

Закрыто для изменения означает что когда модуль был разработан и протестирован, код в нем должен изменяться только что исправления багов.

Открытость для изменения означает что должна быть возможность расширять разработанный код для введения новой функциональности без ущерба для уже разработанного кода.

### Примеры
Плохой код
```python
class Customer:
    customer_type = 0

    def get_discount():
        if this.customer_type == 1:
            return 50
        else
            return 10
```
Хороший код
```python
class Customer:
    def get_discount():
        return 10

class GoldCustomer(Customer):
    def get_discount():
        return 50
```
В будущем, когда понадобится новый тип пользователя, нужно будет просто создать новую модель от пользователя, весь остальной код не меняется.

## Liskov Subsitution Principle (LPI)
> Код который использует базовый класс при заменене этого базового класса на его потомка должен функционировать точно также, как если бы ничего не случилось.

Если при создании класса используется зависимость от класса, должна быть возможность передать в этот класс тот класс или один из его потомков __без получения неожиданных результатов__ и __изначальный класс даже не должен подозревать о подмене__.

### Примеры
Плохой код
```python
class Bird:
    def fly(): return "fly"

class Dove(Bird):
    def fly(): return "flap"

class Eagle(Bird):
    def fly(): return "soar"

class Ostrich(Bird):
    def fly(): raise AttributeError("Can`t fly!")

for bird in (Dove(), Eagle(), Ostrich()):
    bird.fly()  # oops..
```
Хороший код
```python
# Основываясь на проблеме что одна из птиц не умеет летать,
# мы должны подумать о том чтобы убрать этот метод из базового класса
class Bird: pass

class FlyingBird(Bird):
    def fly(): return "fly"

class Dove(FlyingBird):
    def fly(): return "flap"

class Eagle(FlyingBird):
    def fly(): return "soar"

class Ostrich(Bird): pass

for flying_bird in (Eagle(), Dove()):
    flying_bird.fly()
```

## Interface Segregation Principle (ISP)
> Клиента не нужно заставлять имплементировать интерфейс который он не использует, а также клиенты не должены зависеть от методов которые они не испльзуют

Часто при создании класса с большим количествои методов и аттрибутов, другим классам которые работают с этим обычно нужен доступ только к одному или двум методам.

### Примеры
Плохой код
```python
# Этот интерфей обязывает делать очень многое
class IBird(metaclass=abc.Meta):
    @abstractmethod
    def walk(): pass
    @abstractmethod
    def fly(): pass
    @abstractmethod
    def talk(): pass

# При этом ни одна из конкретных имплементаций
# не использует все три метода разом
class Dove(IBird):
    def walk(): return "slow"
    def fly(): return "low"
    def talk(): return ""

class Eagle(IBird):
    def walk(): return ""
    def fly(): return "soar"
    def talk(): return ""

class Parrot(IBird):
    def walk(): return "caged"
    def fly(): return ""
    def talk(): return "polly"
```
Хороший код
```python
# Интерфейсы должны быть разделены
class IWlkingBird(metaclass=abc.Meta):
    @abstractmethod
    def walk: pass

class IFlyingBird(metaclass=abc.Meta):
    @abstractmethod
    def fly(): pass

class ITalkingBird(metaclass=abc.Meta):
    @abstractmethod
    def talk(): pass

# Теперь конкретные имплементации должны определять
# только те методы которые им нужны
class Dove(IWalkingBird, IFlyingBird):
    def walk(): return "slow"
    def fly(): return "low"

class Eagle(IFlyingBird):
    def fly(): return "soar"

class Parrot(IWalkingBird, ITalkingBird):
    def walk(): return "caged"
    def talk(): return "polly"
```

## DPI
> Сущности должны зависеть от абстракций а не конкретных имплементаций. Один высокоуровневый модкль не должен зависеть от другого низкоуровнего модуля, но они должны опираться на абстракции.

DIP в основном относится к концепции слоев приложения, где нижний слой взаимодействует с очень конкретными сущностями, а высшие слои используют нижние классы для достидения более крцпных целей.

Принцип говорит о том, что записимости которые есть между классами должны быть описаны в таких абстракциях как интерфейсы а не через прямое упоминание классов. Часто DIP встречается при dependency injection

### Примеры
Плохой код
```python
class CustomerService:
    
    def activate_login(self, customer):
        log = TextFileLogger()
        log.LogEvent("Customer %s been activated" % customer)
        email_service = MailChimpEmailService()
        email_service.send_welcome_email(customer)
```

Хороший код
```python
# Create interfaces
class ILogger:
    def log_event(event):
        raise NotImplementedError()

class IMailService:
    def send_welcome_email(customer):
        raise NotImplementedError()

# Concrete implementations
class TextFileLogger(ILogger):
    def log_event(event):
        """Writes file to disc."""

class MailChimpEmailService(IMailService):
    def send_welcome_email(customer):
        """Connects to api end sends email."""

# Customer class should not rely on the concrete implementations,
# but rather the provided interfaces

class CustomerService:
    def __init__(self, logger, mailer):
        self._logger = logger
        self.mailer = mailer

    def activate_login(customer):
        self._logger.log_event('Error')
        self._mailer.send_welcome_email(customer)
```