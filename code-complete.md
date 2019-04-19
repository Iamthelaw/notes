# Code complete notes

## Chapter 3 Measure Twice, Cut Once: Upstream Prerequisites

### 3.1 Importance of Prerequisites

#### Do Prerequisites Apply to Modern Software Projects?

By far the most common project risks in software development are poor requirements
and poor project planning, thus preparation tends to focus on improving requirements
and project plans.

#### Causes of Incomplete Preparatio

This phenomenon is known as the WISCA or WIMP syndrome:
Why Isn’t Sam Coding Anything? or Why Isn’t Mary Programming

Put an old program listing on the corner of your desk. Then go right ahead and develop your
requirements and architecture, with or without your boss’s approval. You’ll do the
project faster and with higher-quality results.

Studies over the last 25 years have proven conclusively that it pays to do things right
the first time. **Unnecessary changes are expensive.**

### 3.3 Problem-Definition Prerequisite

The first prerequisite you need to fulfill before beginning construction is a clea
statement of the problem that the system is supposed to solve. This is sometimes called
“product vision,” “vision statement,” “mission statement,” or “product definition.”
Here it’s called “problem definition.”

### 3.4 Requirements Prerequisit

#### Why Have Official Requirements?

Explicit requirements keep you from guessing what the user wants.
Explicit requirements also help to avoid arguments.

#### Handling Requirements Changes During Construction

If you’re driving from Chicago to Los Angeles, is it a waste of
time to stop and look at a road map when you see signs for New York? No. If you’re
not heading in the right direction, stop and check your course.

#### Checklist: Requirements

##### Specific Functional Requirements
- [ ] Are all the inputs to the system specified, including their source,
  accuracy, range of values, and frequency?
- [ ] Are all the outputs from the system specified, including their destination,
  accuracy, range of values, frequency, and format?
- [ ] Are all output formats specified for Web pages, reports, and so on?
- [ ] Are all the external hardware and software interfaces specified?
- [ ] Are all the external communication interfaces specified, including handshaking,
  error-checking, and communication protocols?
- [ ] Are all the tasks the user wants to perform specified?
- [ ] Is the data used in each task and the data resulting from each task specified?

##### Specific Nonfunctional (Quality) Requirements
- [ ] Is the expected response time, from the user’s point of view,
  specified for all necessary operations?
- [ ] Are other timing considerations specified, such as processing time,
  datatransfer rate, and system throughput?
- [ ] Is the level of security specified?
- [ ] Is the reliability specified, including the consequences of software failure,
  the vital information that needs to be protected from failure, and the strategy
  for error detection and recovery?
- [ ] Are minimum machine memory and free disk space specified?
- [ ] Is the maintainability of the system specified,
  including its ability to adapt to changes in specific functionality,
  changes in the operating environment, and changes in its interfaces with other software?
- [ ] Is the definition of success included? Of failure?

##### Requirements Quality
- [ ] Are the requirements written in the user’s language? Do the users think so?
- [ ] Does each requirement avoid conflicts with other requirements?
- [ ] Are acceptable tradeoffs between competing attributes specified - for example,
  between robustness and correctness?
- [ ] Do the requirements avoid specifying the design?
- [ ] Are the requirements at a fairly consistent level of detail?
  Should any requirement be specified in more detail?
  Should any requirement be specified in less detail?
- [ ] Are the requirements clear enough to be turned over to
  an independent group for construction and still be understood? Do the developers think so?
- [ ] Is each item relevant to the problem and its solution?
  Can each item be traced to its origin in the problem environment?
- [ ] Is each requirement testable? Will it be possible for independent testing
  to determine whether each requirement has been satisfied?
- [ ] Are all possible changes to the requirements specified,
  including the likelihood of each change?

##### Requirements Completeness
- [ ] Where information isn’t available before development begins,
  are the areas of incompleteness specified?
- [ ] Are the requirements complete in the sense that if the product satisfies every requirement,
  it will be acceptable?
- [ ] Are you comfortable with all the requirements?
  Have you eliminated requirements that are impossible to implement and included
  just to appease your customer or your boss

### 3.5 Architecture Prerequisite

#### Program Organization

In the architecture, you should find evidence that alternatives to the final organization
were considered and find the reasons for choosing the final organization over its alternatives.
It’s frustrating to work on a class when it seems as if the class’s role in the system
has not been clearly conceived.

Each building block is a class, or it’s a collection of classes or routines that work together
on high-level functions such as interacting with the user, displaying Web pages,
interpreting commands, encapsulating business rules, or accessing data.
Every feature listed in the requirements should be covered by at least one building block.

What each building block is responsible for should be well defined. A building block
should have one area of responsibility, and it should know as little as possible about
other building blocks’ areas of responsibility. By minimizing what each building block
knows about the other building blocks, you localize information about the design into
single building blocks.

#### Major Classes

Aim for the 80/20 rule: specify the 20 percent of
the classes that make up 80 percent of the system’s behavior (Jacobsen, Booch, and
Rumbaugh 1999; Kruchten 2000).

#### Data Design

The architecture should explain why a single database is preferable to
multiple databases (or vice versa), explain why a database is preferable to flat files,
identify possible interactions with other programs that access the same data, explain
what views have been created on the data, and so on.

#### Overengineering

Specifying an approach to overengineering is particularly important because **many
programmers overengineer their classes automatically, out of a sense of professional
pride**. By setting expectations explicitly in the architecture, you can avoid the phenomenon
in which some classes are exceptionally robust and others are barely adequate.

#### Buy-vs.-Build Decisions

The most radical solution to building software is not to build it at all—to buy it instead
or to download open-source software for free. 

#### Checklist: Architecture

##### Specific Architectural Topics
- [ ] Is the overall organization of the program clear,
  including a good architectural overview and justification?
- [ ] Are major building blocks well defined, including their areas of responsibility
  and their interfaces to other building blocks?
- [ ] Are all the functions listed in the requirements covered sensibly,
  by neither too many nor too few building blocks?
- [ ] Are the most critical classes described and justified?
- [ ] Is the data design described and justified?
- [ ] Is the database organization and content specified?
- [ ] Are all key business rules identified and their impact on the system described?
- [ ] Is a strategy for the user interface design described?
- [ ] Is the user interface modularized so that changes
  in it won’t affect the rest of the program?
- [ ] Is a strategy for handling I/O described and justified?
- [ ] Are resource-use estimates and a strategy for resource management
  described and justified for scarce resources like threads, database connections, handles,
  network bandwidth, and so on?
- [ ] Are the architecture’s security requirements described?
- [ ] Does the architecture set space and speed budgets for each class,
  subsystem, or functionality area?
- [ ] Does the architecture describe how scalability will be achieved?
- [ ] Does the architecture address interoperability?
- [ ] Is a strategy for internationalization/localization described?
- [ ] Is a coherent error-handling strategy provided?
- [ ] Is the approach to fault tolerance defined (if any is needed)?
- [ ] Has technical feasibility of all parts of the system been established?
- [ ] Is an approach to overengineering specified?
- [ ] Are necessary buy-vs.-build decisions included?
- [ ] Does the architecture describe how reused code will be made to conform
  to other architectural objectives?
- [ ] Is the architecture designed to accommodate likely changes?

##### General Architectural Quality
- [ ] Does the architecture account for all the requirements?
- [ ] Is any part overarchitected or underarchitected?
  Are expectations in this area set out explicitly?
- [ ] Does the whole architecture hang together conceptually?
- [ ] Is the top-level design independent of the machine and language
  that will be used to implement it?
- [ ] Are the motivations for all major decisions provided?
- [ ] Are you, as a programmer who will implement the system, comfortable with the architecture?

### 3.6 Amount of Time to Spend on Upstream Prerequisites

Generally, a well-run project devotes about 10 to 20 percent of its effort
and about 20 to 30 percent of its schedule to requirements, architecture,
and up-front planning (McConnell 1998, Kruchten 2000).

>  If necessary, plan the architecture work as a separate project, too.

#### Key points

- The overarching **goal of preparing for construction is risk reduction**. Be sure
  your preparation activities are reducing risks, not increasing them.
- If you want to develop high-quality software, attention to quality must be part of
  the software-development process from the beginning to the end. Attention to
  quality at the beginning has a greater influence on product quality than attention at the end.
- Part of a programmer’s job is to educate bosses and coworkers about the software-development
  process, including the importance of adequate preparation before programming begins.
- The kind of project you’re working on significantly affects construction prerequisites
  - many projects should be highly iterative, and some should be more sequential.
- If a good problem definition hasn’t been specified, you might be solving the
  wrong problem during construction.
- If good requirements work hasn’t been done, you might have missed important
  details of the problem. Requirements changes cost 20 to 100 times as much in
  the stages following construction as they do earlier, so be sure the requirements
  are right before you start programming.
- If a good architectural design hasn’t been done, you might be solving the right
  problem the wrong way during construction. The cost of architectural changes
  increases as more code is written for the wrong architecture, so be sure
  the architecture is right, too.
- Understand what approach has been taken to the construction prerequisites on
  your project, and choose your construction approach accordingly.
  
## Chapter 4 Key Construction Decisions

### 4.4 Selection of Major Construction Practice

Some projects use pair programming and test-first development,
while others use solo development and formal inspections. Either combination
of techniques can work well, depending on specific circumstances of the project.

#### Checklist: Major Construction Practices

##### Coding
- [ ] Have you defined how much design will be done up front and how much
  will be done at the keyboard, while the code is being written?
- [ ] Have you defined coding conventions for names, comments, and layout?
- [ ] Have you defined specific coding practices that are implied by the architecture,
  such as how error conditions will be handled, how security will be
  addressed, what conventions will be used for class interfaces, what standards
  will apply to reused code, how much to consider performance while coding, and so on?
- [ ] Have you identified your location on the technology wave and adjusted
  your approach to match? If necessary, have you identified how you will
  program into the language rather than being limited by programming in it?
  
##### Teamwork
- [ ] Have you defined an integration procedure—that is, have you defined the
  specific steps a programmer must go through before checking code into the master sources?
- [ ] Will programmers program in pairs, or individually, or some combination of the two?

##### Quality Assurance
- [ ] Will programmers write test cases for their code before writing the code itself?
- [ ] Will programmers write unit tests for their code regardless of whether
  they write them first or last?
- [ ] Will programmers step through their code in the debugger before they check it in?
- [ ] Will programmers integration-test their code before they check it in?
- [ ] Will programmers review or inspect each other’s code?

##### Tools
- [ ] Have you selected a revision control tool?
- [ ] Have you selected a language and language version or compiler version?
- [ ] Have you selected a framework such as J2EE or Microsoft .NET
  or explicitly decided not to use a framework?
- [ ] Have you decided whether to allow use of nonstandard language features?
- [ ] Have you identified and acquired other tools you’ll be using - editor,
  refactoring tool, debugger, test framework, syntax checker, and so on?

#### Key Points

- Every programming language has strengths and weaknesses. Be aware of the
  specific strengths and weaknesses of the language you’re using.
- Establish programming conventions before you begin programming. It’s nearly
  impossible to change code to match them later.
- More construction practices exist than you can use on any single project.
  Consciously choose the practices that are best suited to your project.
- Ask yourself whether the programming practices you’re using are a response to
  the programming language you’re using or controlled by it.
  Remember to program into the language, rather than programming in it.
- Your position on the technology wave determines what approaches will be
  effective - or even possible. Identify where you are on the technology wave, and
  adjust your plans and expectations accordingly

## Chapter 5 Design in Construction

> “Design” might be just writing a class interface in pseudocode before writing the details.
> It might be drawing diagrams of a few class relationships before coding them.
> It might be asking another programmer which design pattern seems like a better choice.

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

If minimizing development time is more important, a good designer will craft a different design.

#### Design Involves Restrictions

The point of design is partly to create possibilities and partly to **restrict possibilities**.

#### Design Is a Heuristic Process

Because design is nondeterministic, design techniques tend to be heuristics - **“rules of
thumb” or “things to try that sometimes work”** - rather than repeatable processes that
are guaranteed to produce predictable results. **Design involves trial and error**.

### 5.2 Key Design Concepts

#### Software’s Primary Technical Imperative: Managing Complexity

##### Importance of Managing Complexity

Managing complexity is the most important technical topic in software development.
In my view, it’s so important that Software’s Primary Technical Imperative has to be
_managing complexity_.

> One symptom that you have bogged down in complexity overload is when you find
> yourself doggedly applying a method that is clearly irrelevant, at least to any outside observer.
> It is like the mechanically inept person whose car breaks down - so he puts water in the battery
> and empties the ashtrays.

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

- Minimize the amount of essential complexity that anyone’s brain has to deal with at any one time.
- Keep accidental complexity from needlessly proliferating.

#### Desirable Characteristics of a Design

> When I am working on a problem I never think about beauty.
> I think only how to solve the problem. But when I have finished,
> if the solution is not beautiful, I know it is wrong. (R. Buckminster Fuller)

List of internal design characteristics:

- **Minimal complexity** The primary goal of design should be to minimize complexity
  for all the reasons just described. **Avoid making “clever” designs**.
- **Ease of maintenance** This means designing for the maintenance
  programmer. **Continually imagine the questions a maintenance programmer would
  ask about the code you’re writing**.
- **Loose coupling** This means designing so that you hold connections
  among different parts of a program to a minimum.
  Minimal connectedness minimizes work during integration, testing, and maintenance.
- **Extensibility** This means that you can change a piece of a system without
  affecting other pieces.
- **Portability** This means designing the system so that you can easily move it to
  another environment.
- **Leanness** This means designing the system so that it has no extra parts.
  **Extra code has to be developed, reviewed, tested, and considered when the other code is modified**.
  Fatal question: “It’s easy, so what will we hurt by putting it in?” :(
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

- How many different parts of the system does a developer need to understand at
  least a little bit to change something in the graphics subsystem?
- What happens when you try to use the business rules in another system?
- What happens when you want to put a new user interface on the system,
  perhaps a command-line UI for test purposes?
- What happens when you want to put data storage on a remote machine

You want to architect your system so that if you pull out a subsystem to use elsewhere,
you won’t have many hoses to reconnect and those hoses will reconnect easily

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
- **Encapsulation** says, “Furthermore, you aren’t allowed
  to look at an object at any other level of detail”

#### Hide Secrets (Information Hiding)

Designing the class interface is an iterative process just like any other aspect of design.
If you don’t get the interface right the first time, try a few more times until it stabilizes.
If it doesn’t stabilize, you need to try a different approach.

Get into the habit of asking “What should I hide?”
You’ll be surprised at how many difficult design issues dissolve before your eyes.

#### Identify Areas Likely to Change

The goal is to isolate unstable areas so that the effect of a change will be limited to one routine,
class, or package.

1. Identify items that seem likely to change
2. Separate items that are likely to change
3. Isolate items that seem likely to change

Here are a few areas that are likely to change:

- Business rules
- Hardware dependencies
- Input and Output
- Nonstandard language features
- Difficult design and construction areas (They might be done poorly, thus need to change)
- Status variables
  
  - Don't use boolean variable as status variable, use an enumerated type instead
  - Use access routines rather then checking the variable directly
  
#### Anticipating Different Degrees of Change

A good technique for identifying areas likely to change is first to identify the minimal
subset of the program that might be of use to the user. The subset makes up the core
of the system and is unlikely to change.

By identifying the core first, you can see which components are really add-ons and
then extrapolate and hide improvements from there.

#### Keep Coupling Loose

Model railroad cars are coupled by opposing hooks that latch
when pushed together. Connecting two cars is easy—you just push the cars together.
The coupling of model railroad cars works because it’s as simple
as possible. In software, make the connections among modules as simple as possible.

##### Coupling Criteria

- **Size** Number of connections between modules
- **Visibility** Passing data in a parameter list is making an obvious connection and is
  therefore good.
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

Classes and routines are first and foremost intellectual tools for reducing complexity.
If they’re not making your job simpler, they’re not doing their jobs.

#### Look for Common Design Patterns

One potential trap with patterns is force-fitting code to use a pattern.
In some cases, shifting code slightly to conform to a well-recognized pattern
will improve understandability of the code.
But if the code has to be shifted too far,
forcing it to look like a standard pattern can sometimes increase complexity.

#### Other Heuristics

##### Aim for Strong Cohesion

Cohesion refers to how closely all the routines in a class or all the code in
a routine support a central purpose—how focused the class is. Cohesion is a useful tool
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

One of the most effective guidelines is not to get stuck on a single approach.
If diagramming the design in UML isn’t working, write it in English.
Write a short test program. Try a completely different approach. Think of a brute-force solution.
Keep outlining and sketching with your pencil, and your brain will follow. If all else fails,
walk away from the problem. Literally go for a walk, or think about something else
before returning to the problem. 

Some people are uncomfortable if they
don’t come to closure after a design cycle, but after you have created a few designs
without resolving issues prematurely, it will seem natural to leave issues unresolved
until you have more information (Zahniser 1992, Beck 2000).

### 5.4 Design Practices

#### Iterate

You might have had an experience in which you learned so much from writing a program that you wished you could write it again, armed with the insights you gained
from writing it the first time. Design is an iterative process. You don’t usually go from point A only to point B; you
go from point A to point B and back to point A.

Switching from one view of a system to another is
mentally strenuous, but it’s essential to creating effective designs. When you come up
with a first design attempt that seems good enough, don’t stop!
The second attempt is nearly always better than the first, and you learn things on each
attempt that can improve your overall design.

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

- _Insert design documentation into the code itself_ it improves the chance that programmers
  will keep the design documentation reasonably up to date
- _Capture design discussions and desicions on a Wiki_
- _Write e-mail summaries_
- _Use a digital camera_ Taking pictures of whiteboard drawings with a digital camera
  and then embedding those pictures into traditional documents can be a low-effort way
  to get 80 percent of the benefit of saving design drawings by doing about 1 percent of the work
  required if you use a drawing tool.
- _Use CRC (Class, Responsibility, Collaborator) cards_ Another low-tech alternative
  for documenting designs is to use index cards. On each card, designers write a class
  name, responsibilities of the class, and collaborators (other classes that cooperate
  with the class).
- _Create UML disagrams at **appropriate** levels of detail_

### 5.5 Comments on Popular Methodologies

### Checklist: Design in Construction

#### Design Practices
- [ ] Have you iterated, selecting the best of several attempts rather than the first attempt?
- [ ] Have you tried decomposing the system in several different ways to see
  which way will work best?
- [ ] Have you approached the design problem both from the top down and from the bottom up?
- [ ] Have you prototyped risky or unfamiliar parts of the system, creating the
  absolute minimum amount of throwaway code needed to answer specific questions?
- [ ] Has your design been reviewed, formally or informally, by others?
- [ ] Have you driven the design to the point that its implementation seems obvious?
- [ ] Have you captured your design work using an appropriate technique such
  as a Wiki, e-mail, flip charts, digital photography, UML, CRC cards, or
  comments in the code itself?

#### Design Goals
- [ ] Does the design adequately address issues that were identified and
  deferred at the architectural level?
- [ ] Is the design stratified into layers?
- [ ] Are you satisfied with the way the program has been decomposed into
  subsystems, packages, and classes?
- [ ] Are you satisfied with the way the classes have been decomposed into routines?
- [ ] Are classes designed for minimal interaction with each other?
- [ ] Are classes and subsystems designed so that you can use them in other systems?
- [ ] Will the program be easy to maintain?
- [ ] Is the design lean? Are all of its parts strictly necessary?
- [ ] Does the design use standard techniques and avoid exotic, hard-to-understand elements?
- [ ] Overall, does the design help minimize both accidental and essential complexity?

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
  
Anytime you find yourself looking at a class’s implementation to figure out how to use the class,
you’re not programming to the interface; you’re programming through the interface to
the implementation.

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

When I see a base class that has only one derived class, I suspect that some programmer has been
“designing ahead”—trying to anticipate future needs, usually without fully understanding
what those future needs are. The best way to prepare for future work is not to
design extra layers of base classes that “might be needed someday”;
it’s to make current work as clear, straightforward, and simple as possible.
That means not creating any more inheritance structure than is absolutely necessary

##### Be suspicious of classes that override a routine and do nothing inside the derived routine

The place to fix this problem is not in the base class, but in the original Cat class. Create a Claws class and contain that within the Cats class. The root problem was the
assumption that all cats scratch, so fix that problem at the source, rather than just
bandaging it at the destination.

##### Avoid deep inheritance trees

Arthur Riel suggests limiting inheritance hierarchies to a maximum of six levels.
Riel bases his recommendation on the “magic number 7±2,” but I think that’s grossly optimistic.
In my experience most people have trouble juggling more than two or three levels of inheritance in
their brains at once.

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

- _Keep the number of routines in a class as small as possible_
- _Disallow implicitly generated member functions and operators you don’t want_
- _Minimize the number of different routines called by a class_
- _Minimize indirect routine calls to other classes_ Direct connections are hazardous
  enough. Indirect connections - such as
  `account.ContactPerson().DaytimeContactInfo().PhoneNumber()` even more so
- _In general, minimize the extent to which a class collaborates with other classes_

#### Constructors

- _Initialize all member data in all constructors, if possible_  Initializing all data members
  in all constructors is an inexpensive defensive programming practice.
- _Prefer deep copies to shallow copies until proven otherwise_

>  A small number of objects might cause performance issues, but programmers are notoriously poor
at guessing which code really causes problems.

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
1. **Facilitate reusable code** Even if a section of code is called from only one place in the program and is understandable as
    part of a larger class, it makes sense to put it into its own class if that piece of code
    might be used in another program.
    > Notably, the core of NASA’s approach to creating reusable classes does not involve
    “designing for reuse.” NASA identifies reuse candidates at the ends of their projects.
    They then perform the work needed to make the classes reusable as a special project
    at the end of the main project or as the first step in a new project. This approach helps
    prevent “gold-plating”—creation of functionality that isn’t required
    and that unnecessarily adds complexity.
1. **Plan for a family of programs** Thinking through not just what one
    program will look like but what the whole family of programs might look like is a
    powerful heuristic for anticipating entire categories of changes (Parnas 1976).
1. Package related operations
1. Accomplish a specific refactoring

#### Classes to Avoid

- Avoid creating god classes
- Eliminate irrelevant classes
- Avoid classes named after verbs (A class that has only behavior but no data
    is generally not really a class.)

### Checklist: Class Quality

#### Abstract Data Types
- [ ] Have you thought of the classes in your program as abstract data types
    and evaluated their interfaces from that point of view?

#### Abstraction
- [ ] Does the class have a central purpose?
- [ ] Is the class well named, and does its name describe its central purpose?
- [ ] Does the class’s interface present a consistent abstraction?
- [ ] Does the class’s interface make obvious how you should use the class?
- [ ] Is the class’s interface abstract enough that you don’t have to think about
    how its services are implemented? Can you treat the class as a black box?
- [ ] Are the class’s services complete enough that other classes don’t have to
    meddle with its internal data?
- [ ] Has unrelated information been moved out of the class?
- [ ] Have you thought about subdividing the class into component classes,
    and have you subdivided it as much as you can?
- [ ] Are you preserving the integrity of the class’s interface as you modify the class?

#### Encapsulation
- [ ] Does the class minimize accessibility to its members?
- [ ] Does the class avoid exposing member data?
- [ ] Does the class hide its implementation details from other classes as much
    as the programming language permits?
- [ ] Does the class avoid making assumptions about its users, including its derived classes?
- [ ] Is the class independent of other classes? Is it loosely coupled?

#### Inheritance
- [ ] Is inheritance used only to model “is a” relationships—that is, do derived
    classes adhere to the Liskov Substitution Principle?
- [ ] Does the class documentation describe the inheritance strategy?
- [ ] Do derived classes avoid “overriding” non-overridable routines?
- [ ] Are common interfaces, data, and behavior as high as possible in the inheritance tree?
- [ ] Are inheritance trees fairly shallow?
- [ ] Are all data members in the base class private rather than protected?

#### Other Implementation Issues
- [ ] Does the class contain about seven data members or fewer?
- [ ] Does the class minimize direct and indirect routine calls to other classes?
- [ ] Does the class collaborate with other classes only to the extent absolutely necessary?
- [ ] Is all member data initialized in the constructor?
- [ ] Is the class designed to be used as deep copies rather than shallow copies
    unless there’s a measured reason to create shallow copies?

#### Language-Specific Issues
- [ ] Have you investigated the language-specific issues for classes in your
    specific programming language?
    
## Chapter 7 High-Quality Routines

-  The routine’s input variable, inputRec, is changed. If it’s an input variable, its
    value should not be modified
- The routine reads and writes global variables (don't)
- The routine doesn’t have a single purpose
- The routine doesn’t defend itself against bad data
- The routine uses several magic numbers: 100, 4.0, 12, 2, and 3
- Some of the routine’s parameters are unused
- The routine has too many parameters. The upper limit for an understandable
    number of parameters is about 7

### 7.1 Valid Reasons to Create a Routine

1. **Reduce complexity**  The single most important reason to create a routine is to reduce
    a program’s complexity. But after it’s written, you should be able to forget the details
    and use the routine without any knowledge of its internal workings. One indication
    that a routine needs to be broken out of another routine is deep nesting of an inner loop
    or a conditional.
1. **Introduce an intermediate, understandable abstraction** Putting a section of code
    into a well-named routine is one of the best ways to document its purpose.
1. Avoid duplicate code
1. **Support subclassing** You need less new code to override a short, well-factored routine
    than a long, poorly factored routine.
1. Improve portability
1. **Simplify complicated boolean tests**
1. Improve performance
1. **To ensure all routines are small?** No. With so many good reasons for putting code
    into a routine, this one is unnecessary.
    
#### Operations That Seem Too Simple to Put Into Routines

Constructing a whole routine to contain two or three lines of code might seem like overkill,
but experience shows how helpful a good small routine can be. This example hints at another reason
to put small operations into functions: small operations tend to turn into larger operations.

### 7.2 Design at the Routine Level

Several other kinds of cohesion are normally considered to be less than ideal:

- _Sequential cohesion_ exists when a routine contains operations that must be performed
    in a specific order, that share data from step to step, and that don’t make
    up a complete function when done together
- _Communicational cohesion_ occurs when operations in a routine make use of the
    same data and aren’t related in any other way. If a routine prints a summary
    report and then reinitializes the summary data passed into it, the routine has
    communicational cohesion: the two operations are related only by the fact that
    they use the same data
- _Temporal cohesion_ occurs when operations are combined into a routine because
    they are all done at the same time
- _Procedural cohesion_ occurs when operations in a routine are done in a specified order.
- _Logical cohesion_ occurs when several operations are stuffed into the same routine
    and one of the operations is selected by a control flag that’s passed in.
- _Coincidental cohesion_ occurs when the operations in a routine have no discernible
    relationship to each other.
    
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

- list the parameters that are input-only first, input-and-output second, and output-only third
- If several routines use similar parameters, put the similar parameters in a consistent order
- Use all the parameters
- Don’t use routine parameters as working variables
- Put status or error variables last
- Document interface assumptions about parameters. If you assume the data being
    passed to your routine has certain characteristics, document the assumptions as you
    make them. Even better than commenting your assumptions, use assertions to put them into code.
- Limit the number of a routine’s parameters to about seven. If you are passing the same data
    to many different routines, group the routines into a class and treat the frequently used data
    as class data.
- Pass the variables or objects that the routine needs to maintain its interface abstraction.
    There are two competing schools of thought about how to pass members of an object to a routine.
    
    - Proponents of the first school of thought argue that only the three specific elements
        needed by the routine should be passed. They argue that doing this will keep
        the connections between routines to a minimum; reduce coupling; and make them easier to
        understand, reuse, and so on. They say that passing the whole object to a routine
        violates the principle of encapsulation by potentially exposing all 10 access routines to
        the routine that’s called.
    - Proponents of the second school argue that the whole object should be passed. They
        argue that the interface can remain more stable if the called routine has the flexibility
        to use additional members of the object without changing the routine’s interface.
        They argue that passing three specific elements violates encapsulation by exposing
        which specific data elements the routine is using.
        
    If you find yourself frequently changing the parameter list to the routine, with the
    parameters coming from the same object each time, that’s an indication that you
    should be passing the whole object rather than specific elements.
    
### 7.6 Special Considerations in the Use of Functions

> A function is a routine that returns a value; a procedure is a routine that does not.

#### When to Use a Function and When to Use a Procedure

The function would always be named for the value
it returned, as sin(), CustomerID(), and ScreenHeight() are. A procedure, on the other
hand, could take input, modify, and output parameters—as many of each as it wanted to.

A common programming practice is to have a function that operates as a procedure and
returns a status value. The alternative is to create a procedure that has a status variable
as an explicit parameter.

### Checklist: High-Quality Routines

#### Big-Picture Issues
- [ ] Is the reason for creating the routine sufficient?
- [ ] Have all parts of the routine that would benefit from being put into routines of their own been put into routines of their own?
- [ ] Is the routine’s name a strong, clear verb-plus-object name for a procedure
    or a description of the return value for a function?
- [ ] Does the routine’s name describe everything the routine does?
- [ ] Have you established naming conventions for common operations?
- [ ] Does the routine have strong, functional cohesion—doing one and only
    one thing and doing it well?
- [ ] Do the routines have loose coupling—are the routine’s connections to
    other routines small, intimate, visible, and flexible?
- [ ] Is the length of the routine determined naturally by its function and logic,
    rather than by an artificial coding standard?

#### Parameter-Passing Issues
- [ ] Does the routine’s parameter list, taken as a whole, present a consistent
    interface abstraction?
- [ ] Are the routine’s parameters in a sensible order, including matching the
    order of parameters in similar routines?
- [ ] Are interface assumptions documented?
- [ ] Does the routine have seven or fewer parameters?
- [ ] Is each input parameter used?
- [ ] Is each output parameter used?
- [ ] Does the routine avoid using input parameters as working variables?
- [ ] If the routine is a function, does it return a valid value under all possible circumstances?

## Chapter 8 Defensive Programming

> In defensive driving, you adopt the mind-set that you’re never sure
what the other drivers are going to do.

### 8.2 Assertions

- That an input parameter’s value falls within its expected range (or an output
    parameter’s value does)
- That a file or stream is open (or closed) when a routine begins executing (or
    when it ends executing)
- That a file or stream is at the beginning (or end) when a routine begins executing (or when it ends executing)
- That a file or stream is open for read-only, write-only, or both read and write
- **That the value of an input-only variable is not changed by a routine**
- That a pointer is non-null
- That an array or other container passed into a routine can contain at least X
    number of data elements
- That a table has been initialized to contain real values
- That a container is empty (or full) when a routine begins executing (or when it finishes)
- That the results from a highly optimized, complicated routine match the results
    from a slower but clearly written routine
    
During production, they can be compiled out of the code so that
the assertions don’t degrade system performance.

#### Guidelines for Using Assertions

> Use error-handling code for conditions you expect to occur; use assertions for
conditions that should never occur

For highly robust code, assert and then handle the error anyway.

### 8.3 Error-Handling Techniques

- Return a neutral value. A drawing routine that displays x-ray data for cancer patients, however, would not want to
    display a “neutral value.” In that case, you’d be better off shutting down the program
    than displaying incorrect patient data.
- Substitute the next piece of valid data. If you’re taking readings from a thermometer 100
    times per second and you don’t get a valid reading one time, you might simply wait
    another 1/100th of a second and take the next reading.
- Return the same answer as the previous time 
- Substitute the closest legal value
- Log a warning message to a file 
- Return an error code 
- Call an error-processing routine/object
- Display an error message wherever the error is encountered. Attackers
    sometimes use error messages to discover how to attack a system.
- Handle the error in whatever way works best locally
- Shut down

#### Robustness vs. Correctness

**Correctness** means never returning an inaccurate result;
returning no result is better than returning an inaccurate result.

**Robustness** means always trying to do something that will allow the software to keep operating,
even if that leads to results that are inaccurate sometimes.

### 8.4 Exceptions

> Don’t throw an uncaught exception in a section of code if you can handle the error locally

You should always consider the full set of error-handling alternatives: handling the error locally,
propagating the error by using an error code, logging debug information to a file,
shutting down the system, or using some other approach.

Sometimes the best response to a serious run-time error is to release all acquired resources and abort.
Let the user rerun the program with proper input.

### 8.5 Barricade Your Program to Contain the Damage Caused by Errors

The class’s public methods assume
the data is unsafe, and they are responsible for checking the data and sanitizing it.
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

Typically, you won’t go to the effort of writing a debugging aid until after you’ve been bitten
by a problem several times.

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
- [ ] Completely fill any memory allocated so that you can detect memory allocation errors
- [ ] Completely fill any files or streams allocated to flush out any file-format errors
- [ ] Be sure the code in each case statement’s default or else clause fails hard (aborts
    the program) or is otherwise impossible to overlook
- [ ] Fill an object with junk data just before it’s deleted
- [ ] Set up the program to e-mail error log files to yourself so that you can see the
    kinds of errors that are occurring in the released software, if that’s appropriate
    for the kind of software you’re developing

Sometimes the best defense is a good offense. Fail hard during development so that
you can fail softer during production.

### 8.8 Being Defensive About Defensive Programming

Too much defensive programming creates problems of its own. If you check data
passed as parameters in every conceivable way in every conceivable place,
your program will be fat and slow. What’s worse, the additional code needed for defensive programming
adds complexity to the software. Code installed for defensive
programming is not immune to defects, and you’re just as likely to find a defect in
defensive-programming code as in any other code - more likely, if you write the code
casually.

### Checklist: Defensive Programming

#### General
- [ ] Does the routine protect itself from bad input data?
- [ ] Have you used assertions to document assumptions, including preconditions and postconditions?
- [ ] Have assertions been used only to document conditions that should never occur?
- [ ] Does the architecture or high-level design specify a specific set of errorhandling techniques?
- [ ] Does the architecture or high-level design specify whether error handling
    should favor robustness or correctness?
- [ ] Have barricades been created to contain the damaging effect of errors and
    reduce the amount of code that has to be concerned about error processing?
- [ ] Have debugging aids been used in the code?
- [ ] Have debugging aids been installed in such a way that they can be activated
    or deactivated without a great deal of fuss?
- [ ] Is the amount of defensive programming code appropriate—neither too much nor too little?
- [ ] Have you used offensive-programming techniques to make errors difficult
    to overlook during development?

#### Exceptions
- [ ] Has your project defined a standardized approach to exception handling?
- [ ] Have you considered alternatives to using an exception?
- [ ] Is the error handled locally rather than throwing a nonlocal exception, if possible?
- [ ] Does the code avoid throwing exceptions in constructors and destructors?
- [ ] Are all exceptions at the appropriate levels of abstraction for the routines that throw them?
- [ ] Does each exception include all relevant exception background information?
- [ ] Is the code free of empty catch blocks? (Or if an empty catch block truly is
    appropriate, is it documented?)212 Chapter 8: Defensive Programming

#### Security Issues
- [ ] Does the code that checks for bad input data check for attempted buffer
    overflows, SQL injection, HTML injection, integer overflows, and other malicious inputs?
- [ ] Are all error-return codes checked?
- [ ] Are all exceptions caught?
- [ ] Do error messages avoid providing information that would help an
    attacker break into the system?
    
## Chapter 9 The Pseudocode Programming Process

### 9.1 Summary of Steps in Building Classes and Routines

#### Steps in Creating a Class

- Create a general design for the class
    1. Define the class’s specific responsibilities
    1. Define what “secrets” the class will hide
    1. Define exactly what abstraction the class interface will capture
    1. Determine whether the class will be derived from another class
        and whether other classes will be allowed to derive from it.
    1. Identify the class’s key public methods
    1. Identify and design any nontrivial data members used by the class
- Construct each routine within the class
- Review and test the class as a whole

### 9.2 Pseudocode for Pros

Here are guidelines for using pseudocode effectively:

- Use English-like statements that precisely describe specific operations
- **Avoid syntactic elements from the target programming language**.
    Pseudocode allows you to design at a slightly higher level than the code itself.
    When you use programming-language constructs, you sink to a lower level, eliminating the
    main benefit of design at a higher level, and you saddle yourself with unnecessary
    syntactic restrictions.
- Write pseudocode at the level of intent. Describe the meaning of the approach
    rather than how the approach will be implemented in the target language.
- Write pseudocode at a low enough level that generating code from it will be nearly automatic.
    If the pseudocode is at too high a level, it can gloss over problematic details in the code.
    Refine the pseudocode in more and more detail until it seems as if it would be
    easier to simply write the code.
    
> When the pseudocode statements are converted to comments, they’ll be a good
explanation of the code’s intent.

Here are the benefits you can expect from using this style of pseudocode:

- Pseudocode makes reviews easier. You can review detailed designs without examining source code
- Pseudocode supports the idea of iterative refinement
- Pseudocode makes changes easier. A few lines of pseudocode are easier to change
than a page of code
- Pseudocode minimizes commenting effort. In the PPP, the pseudocode statements become the comments,
    so it actually takes more work to remove the comments than to leave them in.
- Pseudocode is easier to maintain than other forms of design documentation.
    As long as the inline comments are maintained, the pseudocode’s documentation of the design
    will be accurate.
    
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

The single biggest way to improve both the quality of your code and your productivity is
**to reuse good code**.

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

Once you’ve written the pseudocode and designed the data,
take a minute to review the pseudocode you’ve written. Back away from it, and **think
about how you would explain it to someone else**.

> People are also more willing to review a few lines of
pseudocode than they are to review 35 lines of C++ or Java.

##### Try a few ideas in pseudocode, and keep the best (iterate) 

> Once you start coding, you get emotionally involved with your code and it becomes harder
to throw away a bad design and start over.

If you’re not sure how to code something, keep working with the pseudocode until you are sure.
Keep refining and decomposing the pseudocode until it seems like a waste of time
to write it instead of the actual code.

#### Code the Routine

#### Check the Code

- Mentally check the routine for errors 
- Compile the routine
    After the first compile, you step up the pressure:
    “I’ll get it right with just one more compile.” **“Just One More Compile” syndrome**.
    The point of this book is to show how to rise above the cycle of hacking something
    together and running it to see if it works. 
- Step through the code in the debugger (**Even before the bug**)
- Test the code
- Remove errors from the routine.
    If you find that a routine is unusually buggy, start over. Don’t hack around it - rewrite it.
    Creating an entirely new design for a buggy routine pays off.
    
#### Clean Up Leftovers

- Check the routine’s interface. Make sure that all input and output data is
    accounted for and that all parameters are used
- Check for general design quality. Make sure the routine does one thing and does
    it well, that it’s loosely coupled to other routines, and that it’s designed defensively
- Check the routine’s variables. Check for inaccurate variable names, unused objects,
    undeclared variables, improperly initialized objects, and so on
- Check the routine’s statements and logic. Check for off-by-one errors, infinite loops,
    improper nesting, and resource leaks
- Check the routine’s layout. Make sure you’ve used white space to clarify the logical structure
    of the routine, expressions, and parameter lists
- Check the routine’s documentation. Make sure the pseudocode that was translated into comments
    is still accurate. Check for algorithm descriptions, for documentation on interface assumptions
    and nonobvious dependencies, for justification of unclear coding practices
- Remove redundant comments

### Checklist: The Pseudocode Programming Process
- [ ] Have you checked that the prerequisites have been satisfied?
- [ ] Have you defined the problem that the class will solve?
- [ ] Is the high-level design clear enough to give the class and each of its routines a good name?
- [ ] Have you thought about how to test the class and each of its routines?
- [ ] Have you thought about efficiency mainly in terms of stable interfaces and readable
    implementations or mainly in terms of meeting resource and speed budgets?
- [ ] Have you checked the standard libraries and other code libraries for applicable routines
    or components?
- [ ] Have you checked reference books for helpful algorithms?
- [ ] Have you designed each routine by using detailed pseudocode?
- [ ] Have you mentally checked the pseudocode? Is it easy to understand?
- [ ] Have you paid attention to warnings that would send you back to design (use of global data,
    operations that seem better suited to another class or another routine, and so on)?
- [ ] Did you translate the pseudocode to code accurately?
- [ ] Did you apply the PPP recursively, breaking routines into smaller routines when needed?
- [ ] Did you document assumptions as you made them?
- [ ] Did you remove comments that turned out to be redundant?
- [ ] Have you chosen the best of several iterations, rather than merely stopping after your first
    iteration?
- [ ] Do you thoroughly understand your code? Is it easy to understand?

## Chapter 10 General Issues in Using Variables

### 10.4 Scope

- Initialize variables used in a loop immediately before the loop rather than back at the
    beginning of the routine containing the loop
- Don’t assign a value to a variable until just before the value is used
- **Group related statements**
- Break groups of related statements into separate routines
- Begin with most restricted visibility, and expand the variable’s scope only if
    necessary. It is much more difficult to reduce the scope of a variable that has had a large
    scope than to expand the scope of a variable that has had a small scope.
    It’s harder to turn a protected data member into a private data member than vice versa.
    
### 10.6 Binding Time

>  the greater the flexibility desired, the higher the complexity of the code needed
to support that flexibility and the more error-prone the code will be.
Because successful programming depends on minimizing complexity,
a skilled programmer will build in as much flexibility as
needed to meet the software’s requirements but will not add flexibility—and related
complexity—beyond what’s required.

## Chapter 11 The Power of Variable Names
### 11.1 Considerations in Choosing Good Names
#### The Most Important Naming Consideration

Programmers sometimes overlook using the ordinary words, which is often the easiest solution.

#### Problem Orientation

> A good mnemonic name generally speaks to the problem rather than the solution

A record of employee data could be called `inputRec` or `employeeData`.
inputRec is a computer term that refers to computing ideas - input and record.
`employeeData` refers to the problem domain rather than the computing universe.
Similarly, for a bit field indicating printer status, `bitFlag` is a more computerish name
than `printerReady`. In an accounting application, `calcVal` is more computerish than `sum`.

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

**Think of a better name than flag for status variables** It’s better to think of flags as
status variables. A flag should never have flag in its name because that doesn’t give you
any clue about what the flag does.

> When you find yourself “figuring out” a section of code, consider renaming the variables. It’s OK to figure out murder mysteries, but you shouldn’t need to figure out
code. You should be able to read it.

#### Naming Boolean Variables

Here are some particularly useful boolean variable names:

- done
- error
- found
- success or ok

Some programmers like to put Is in front of their boolean names.

### 11.3 The Power of Naming Conventions

#### Why Have Conventions?

- By making one global decision rather than many local ones,
    you can concentrate on the more important characteristics of the code
- They help you transfer knowledge across projects
- They help you learn code more quickly on a new project
- Without naming conventions, you can easily call the same thing by two different names
- They emphasize relationships among related items

> The key is that any convention at all is often better than no convention.

#### When You Should Have a Naming Convention

- When multiple programmers are working on a project
- When you plan to turn a program over to another programmer for modifications
    and maintenance (**which is nearly always**)
- When your programs are reviewed by other programmers in your organization
- When your program is so large that you can’t hold the whole thing in your brain
    at once and must think about it in pieces
- When the program will be long-lived enough that you might put it aside for a
    few weeks or months before working on it again
- When you have a lot of unusual terms that are common on a project and want to
    have standard terms or abbreviations to use in coding
    
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
standardize on for use in that program. The codes are mnemonics such as `wn` for windows
and `scr` for screen regions.

### 11.7 Kinds of Names to Avoid

- **Avoid misleading names or abbreviations**
- **Avoid names with similar meanings** If you can switch the names of two variables
    without hurting the program, you need to rename both variables. For example, `input`
    and `inputValue`, `recordNum` and `numRecords`, and `fileNumber` and `fileIndex`
- **Avoid variables with different meanings but similar names** Avoid names like
    `clientRecs` and `clientReps`
- **Avoid names that sound similar, such as wrap and rap**
- **Avoid numerals in names**
- **Avoid misspelled words in names**
- **Don’t differentiate variable names solely by capitalization**
- **Avoid multiple natural languages** `color` and `colour`
- **Avoid names containing hard-to-read characters** `ttl5`, `ttlS`, `tt1S`


### Checklist: Naming Variables

#### General Naming Considerations
- [ ] Does the name fully and accurately describe what the variable represents?
- [ ] Does the name refer to the real-world problem rather than to the programming-language solution?
- [ ] Is the name long enough that you don’t have to puzzle it out?
- [ ] Are computed-value qualifiers, if any, at the end of the name?
- [ ] Does the name use Count or Index instead of Num?

#### Naming Specific Kinds of Data
- [ ] Are loop index names meaningful (something other than i, j, or k if the
    loop is more than one or two lines long or is nested)?
- [ ] Have all “temporary” variables been renamed to something more meaningful?
- [ ] Are boolean variables named so that their meanings when they’re true are clear?
- [ ] Do enumerated-type names include a prefix or suffix that indicates the category - for example,
    Color_ for Color_Red, Color_Green, Color_Blue, and so on?
- [ ] Are named constants named for the abstract entities they represent rather
    than the numbers they refer to?

#### Naming Conventions
- [ ] Does the convention distinguish among local, class, and global data?
- [ ] Does the convention distinguish among type names, named constants,
    enumerated types, and variables?
- [ ] Does the convention identify input-only parameters to routines in languages
    that don’t enforce them?
- [ ] Is the convention as compatible as possible with standard conventions for the language?
- [ ] Are names formatted for readability?

#### Short Names
- [ ] Does the code use long names (unless it’s necessary to use short ones)?
- [ ] Does the code avoid abbreviations that save only one character?
- [ ] Are all words abbreviated consistently?Key Points 289
- [ ] Are the names pronounceable?
- [ ] Are names that could be misread or mispronounced avoided?
- [ ] Are short names documented in translation tables?

#### Common Naming Problems: Have You Avoided...
- [ ] ...names that are misleading?
- [ ] ...names with similar meanings?
- [ ] ...names that are different by only one or two characters?
- [ ] ...names that sound similar?
- [ ] ...names that use numerals?
- [ ] ...names intentionally misspelled to make them shorter?
- [ ] ...names that are commonly misspelled in English?
- [ ] ...names that conflict with standard library routine names or with predefined variable names?
- [ ] ...totally arbitrary names?
- [ ] ...hard-to-read characters?

## Chapter 12 Fundamental Data Types

### 12.1 Numbers in General

- Avoid "magic numbers"
- Anticipate divide-by-zero errors
- Avoid mixed-type comparisons 

### 12.2 Integers

- Check for integer division  (The easiest way to remedy this problem is to
    reorder the expression so that the divisions are done last)
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

### Checklist: Fundamental Data

#### Numbers in General
- [ ] Does the code avoid magic numbers?
- [ ] Does the code anticipate divide-by-zero errors?
- [ ] Are type conversions obvious?
- [ ] If variables with two different types are used in the same expression, will
    the expression be evaluated as you intend it to be?
- [ ] Does the code avoid mixed-type comparisons?
- [ ] Does the program compile with no warnings?

#### Integers
- [ ] Do expressions that use integer division work the way they’re meant to?
- [ ] Do integer expressions avoid integer-overflow problems?

#### Floating-Point Numbers
- [ ] Does the code avoid additions and subtractions on numbers with greatly different magnitudes?
- [ ] Does the code systematically prevent rounding errors?
- [ ] Does the code avoid comparing floating-point numbers for equality?

#### Characters and Strings
- [ ] Does the code avoid magic characters and strings?
- [ ] Are references to strings free of off-by-one errors?
- [ ] Does C code treat string pointers and character arrays differently?
- [ ] Does C code follow the convention of declaring strings to be length CONSTANT+1?
- [ ] Does C code use arrays of characters rather than pointers, when appropriate?
- [ ] Does C code initialize strings to NULLs to avoid endless strings?
- [ ] Does C code use strncpy() rather than strcpy()? And strncat() and strncmp()?

#### Boolean Variables
- [ ] Does the program use additional boolean variables to document conditional tests?
- [ ] Does the program use additional boolean variables to simplify conditional tests?

#### Enumerated Types
- [ ] Does the program use enumerated types instead of named constants for
    their improved readability, reliability, and modifiability?
- [ ] Does the program use enumerated types instead of boolean variables
    when a variable’s use cannot be completely captured with true and false?
- [ ] Do tests using enumerated types test for invalid values?
- [ ] Is the first entry in an enumerated type reserved for “invalid”?

#### Named Constants
- [ ] Does the program use named constants for data declarations and loop
    limits rather than magic numbers?
- [ ] Have named constants been used consistently—not used as named constants in some places and as literals in others?

#### Arrays
- [ ] Are all array indexes within the bounds of the array?
- [ ] Are array references free of off-by-one errors?
- [ ] Are all subscripts on multidimensional arrays in the correct order?
- [ ] In nested loops, is the correct variable used as the array subscript,
    avoiding loop-index cross-talk?318 Chapter 12: Fundamental Data Types

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
you might be able to guess that each of these routines
accesses class data. But you can’t know for sure from reading this code.

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
    Because all the routines use expenseData, you have a hint that they might be working
    on the same data and that the order of the statements might be important.
- Document unclear dependencies with comments
- Check for dependencies with assertions or error-handling code
     For example, in the class’s constructor, you might initialize a class member variable
     `isExpenseDataInitialized` to `false`. Then in `InitializeExpenseData()`, you can
     set `isExpenseDataInitialized` to `true`. Each function that depends on `expenseData`
     being initialized can then check whether `isExpenseDataInitialized` has been set to `true`
     before performing additional operations on expenseData.

### 14.2 Statements Whose Order Doesn’t Matter

>  The guiding principle is the Principle of Proximity: Keep related actions together.

#### Making Code Read from Top to Bottom

As a general principle, make the program read from top to bottom rather than jumping around.

### Checklist: Organizing Straight-Line Code
- [ ] Does the code make dependencies among statements obvious?
- [ ] Do the names of routines make dependencies obvious?
- [ ] Do parameters to routines make dependencies obvious?
- [ ] Do comments describe any dependencies that would otherwise be unclear?
- [ ] Have housekeeping variables been used to check for sequential dependencies
    in critical sections of code?
- [ ] Does the code read from top to bottom?
- [ ] Are related statements grouped together?
- [ ] Have relatively independent groups of statements been moved into their own routines?

## Chapter 15 Using Conditionals

### 15.1 if Statements

#### Plain if-then Statements

> Check for reversal of the if and else clauses

#### Chains of if-then-else Statements

- Put the most common cases first 
- Make sure that all cases are covered Code a final else clause with an error message
    or assertion to catch cases you didn’t plan for.
    
### Checklist: Using Conditionals

#### if-then Statements
- [ ] Is the nominal path through the code clear?
- [ ] Do if-then tests branch correctly on equality?
- [ ] Is the else clause present and documented?
- [ ] Is the else clause correct?
- [ ] Are the if and else clauses used correctly—not reversed?
- [ ] Does the normal case follow the if rather than the else?

#### if-then-else-if Chains
- [ ] Are complicated tests encapsulated in boolean function calls?
- [ ] Are the most common cases tested first?
- [ ] Are all cases covered?
- [ ] Is the if-then-else-if chain the best implementation—better than a case statement?

#### `case` Statements
- [ ] Are cases ordered meaningfully?
- [ ] Are the actions for each case simple—calling other routines if necessary?
- [ ] Does the case statement test a real variable, not a phony one that’s made
    up solely to use and abuse the case statement?
- [ ] Is the use of the default clause legitimate?
- [ ] Is the default clause used to detect and report unexpected cases?
- [ ] In C, C++, or Java, does the end of each case have a break?

## Chapter 16 Controlling Loops

### 16.2 Controlling the Loop

#### Entering the Loop

- Put initialization code directly before the loop. The same kind of error can occur when you move or
copy the loop code into a different routine without moving or copying its initialization
code.

### 16.2 Controlling the Loop

#### How Long Should a Loop Be?

- Make your loops short enough to view all at once. You’ll rarely write loops longer
    than 15 or 20 lines.
- **Move loop innards of long loops into routines** If the loop is well designed, the code
    on the inside of a loop can often be moved into one or more routines that are called
    from within the loop.
- Make long loops especially clear

### 16.3 Creating Loops Easily—From the Inside Out

>  Here’s the general process.
Start with one case. Code that case with literals. Then indent it, put a loop around it,
and replace the literals with loop indexes or computed expressions. Put another loop
around that, if necessary, and replace more literals. Continue the process as long as
you have to. When you finish, add all the necessary initializations.

### Chapter 17 Unusual Control Structures

#### 17.2 Recursion

For most problems, it produces massively complicated solutions—in those
cases, simple iteration is usually more understandable.

The typical examples are computing a factorial or computing a Fibonacci sequence. Recursion is
a powerful tool, and it’s really dumb to use it in either of those cases.

Third, and most important, you should consider alternatives to recursion before using it.

### Checklist: Unusual Control Structures

#### `return`
- [ ] Does each routine use return only when necessary?
- [ ] Do returns enhance readability?

#### Recursion
- [ ] Does the recursive routine include code to stop the recursion?
- [ ] Does the routine use a safety counter to guarantee that the routine stops?
- [ ] Is recursion limited to one routine?
- [ ] Is the routine’s depth of recursion within the limits imposed by the size of
    the program’s stack?
- [ ] Is recursion the best way to implement the routine? Is it better than simple iteration

## Chapter 18 Table-Driven Methods

A table-driven method is a scheme that allows you to look up information in a table
rather than using logic statements (if and case) to figure it out.

### 18.1 General Considerations in Using Table-Driven Methods

You put your program’s knowledge into its data rather than into its logic - in the table instead
of in the if tests.

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

More generally, complicated code is a sign that you don’t understand your program
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

### Checklist: Control-Structure Issues

- [ ] Do expressions use true and false rather than 1 and 0?
- [ ] Are boolean values compared to true and false implicitly?
- [ ] Are numeric values compared to their test values explicitly?
- [ ] Have expressions been simplified by the addition of new boolean variables
    and the use of boolean functions and decision tables?
- [ ] Are boolean expressions stated positively?
- [ ] Do pairs of braces balance?
- [ ] Are braces used everywhere they’re needed for clarity?
- [ ] Are logical expressions fully parenthesized?
- [ ] Have tests been written in number-line order?
- [ ] Do Java tests uses a.equals(b) style instead of a == b when appropriate?
- [ ] Are null statements obvious?
- [ ] Have nested statements been simplified by retesting part of the conditional,
    converting to if-then-else or case statements, moving nested code
    into its own routine, converting to a more object-oriented design, or have
    they been improved in some other way?
- [ ] If a routine has a decision count of more than 10, is there a good reason for
    not redesigning it?

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

The attempt to maximize certain characteristics inevitably conflicts with the attempt to
maximize others.

### 20.2 Techniques for Improving Software Quality

- **Software-quality objectives**  One powerful technique for improving software quality
    is setting explicit quality objectives from among the external and internal characteristics.
    The power of setting explicit goals.
- **Explicit quality-assurance activity** The organization must show
    programmers that quality is a priority.
- **Testing strategy**
- **Software-engineering guidelines**
- **Informal technical reviews**
- **Formal technical reviews** Inspection, a peer review, a customer review, or an audit.
- **External audits**

#### Development Process

##### Change-control procedures

One big obstacle to achieving software quality is uncontrolled changes.
Uncontrolled requirements changes can result in disruption to design and coding.
Uncontrolled changes in design can result in code that doesn’t agree with its requirements,
inconsistencies in the code, or more time spent modifying code to meet the changing design
than spent moving the project forward. 

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

The strong implication is that if project developers are striving for a higher defectdetection rate,
they need to use a combination of techniques.
 
Boeing and other companies have reported that different people tend to find different defects.

Glenford Myers points out that human processes (inspections and walk-throughs, for
instance) tend to be better than computer-based testing at finding certain kinds of
errors and that the opposite is true for other kinds of errors (1979). This result was confirmed
in a later study, which found that code reading detected more interface defects and functional
testing detected more control defects (Basili, Selby, and Hutchens 1986)

This data can also be used to understand why programmers who begin working with a
**disciplined defect-removal technique such as Extreme Programming** experience higher
defect-removal levels than they have experienced previously. 

#### Cost of Finding Defects

Most studies have found that inspections are cheaper than testing.

#### Cost of Fixing Defects

The longer a defect remains in the system, the more expensive it
becomes to remove. Even more important, some techniques, such as inspections,
detect the symptoms and causes of defects in one step; others, such as testing, find
symptoms but require additional work to diagnose and fix the root cause.

### 20.4 When to Do Quality Assurance

The earlier an error is inserted into software, the more entangled it becomes in other parts of the
software and the more expensive it becomes to remove. A requirements error can result in
extra architecture or in bad architectural decisions. The extra architecture results in extra code,
test cases, and documentation. It’s a good idea to catch requirements and architecture errors
before they affect later activities.

### 20.5 The General Principle of Software Quality

The best way to improve productivity and quality is to reduce the time spent reworking code,
whether the rework arises from changes in requirements, changes in design, or debugging.

The single biggest activity on most projects is debugging and correcting code that
doesn’t work properly.

It’s not necessarily the case that writing software without defects takes more time
than writing software with defects.

### Checklist: A Quality-Assurance Plan
- [ ] Have you identified specific quality characteristics that are important to your project?
- [ ] Have you made others aware of the project’s quality objectives?
- [ ] Have you differentiated between external and internal quality characteristics?
- [ ] Have you thought about the ways in which some characteristics might
    compete with or complement others?
- [ ] Does your project call for the use of several different error-detection techniques suited to finding several different kinds of errors?
- [ ] Does your project include a plan to take steps to assure software quality
    during each stage of software development?
- [ ] Is the quality measured in some way so that you can tell whether it’s improving or degrading?
- [ ] Does management understand that quality assurance incurs additional costs up front in order
    to save costs later?
    
## Chapter 21 Collaborative Construction

In one way or another, all collaborative construction techniques are attempts to formalize
the process of showing your work to someone else for the purpose of flushing out errors.

### 21.1 Overview of Collaborative Development Practices

Studies at the Software Engineering Institute have
found that developers insert an average of 1 to 3 defects per hour into their designs
and 5 to 8 defects per hour into code (Humphrey 1997), so attacking these blind
spots is a key to effective construction.

#### Collaborative Construction Complements Other Quality-Assurance Techniques

The primary purpose of collaborative construction is to improve software quality. As
noted in Chapter 20, “The Software-Quality Landscape,” software testing has limited
effectiveness when used alone—the average defect-detection rate is only about
30 percent for unit testing, 35 percent for integration testing, and 35 percent for low-volume
beta testing.

As Karl Wiegers points out, “A human reviewer can spot unclear error messages, inadequate comments,
hard-coded variable values, and repeated code patterns that should be consolidated. Testing
won’t” (Wiegers 2002).

#### Collaborative Construction Provides Mentoring in Corporate Culture and Programming Expertise

Reviews create a venue for more experienced and less experienced programmers to
communicate about technical issues. 

#### Collective Ownership Applies to All Forms of Collaborative Construction

Some methodologies, such as Extreme Programming, recommend formally pairing
programmers and rotating their work assignments over time. At my company, we’ve
found that programmers don’t need to pair up formally to achieve good code coverage.

### 21.2 Pair Programming

When pair programming, one programmer types in code at the keyboard and the
other programmer watches for mistakes and thinks strategically about whether the
code is being written correctly and whether the right code is being written.
Pair programming was originally popularized by Extreme Programming (Beck 2000).

#### Keys to Success with Pair Programming

- **Support pair programming with coding standards** Pair programming will not be effective
    if the two people in the pair spend their time arguing about coding style.
- **Don’t let pair programming turn into watching**
- **Don’t force pair programming of the easy stuff**
- **Rotate pairs and work assignments regularly**
- Encourage pairs to match each other’s pace
- Don’t force people who don’t like each other to pair
- Avoid pairing all newbies
- Assign a team leader

#### Benefits of Pair Programming

- It holds up better under stress than solo development. Pairs encourage each
    other to keep code quality high even when there’s pressure to write quick and dirty code.
- It improves code quality. The readability and understandability of the code
    tends to rise to the level of the best programmer on the team.
- It shortens schedules. Pairs tend to write code faster and with fewer errors.
    The project team spends less time at the end of the project correcting defects.
- It produces all the other general benefits of collaborative construction,
    including disseminating corporate culture, mentoring junior programmers,
    and fostering collective ownership.
    
### Checklist: Effective Pair Programming
- Do you have a coding standard so that pair programmers stay focused on
    programming rather than on philosophical coding-style discussions?
- Are both partners participating actively?
- Are you avoiding pair programming everything and, instead, selecting the
    assignments that will really benefit from pair programming?
- Are you rotating pair assignments and work assignments regularly?
- Are the pairs well matched in terms of pace and personality?
- Is there a team leader to act as the focal point for management and other
    people outside the project?
    
### 21.3 Formal Inspections

- Checklists focus the reviewers’ attention on areas that have been problems in the past
- The inspection focuses on **defect detection, not correction**
- Reviewers prepare for the inspection meeting beforehand and arrive with a list
    of the problems they’ve discovered
- Distinct roles are assigned to all participants
- The moderator of the inspection isn’t the author of the work product under inspection
- The moderator has received specific training in moderating inspections
- The inspection meeting is held only if all participants have adequately prepared
- Data is collected at each inspection and is fed into future inspections to improve them
- General management doesn’t attend the inspection meeting unless you’re inspecting
    a project plan or other management materials. Technical leaders might attend

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
It is also self-optimizing because it uses a formal feedback loop to improve the checklists
and to monitor preparation and inspection rates.

### Checklist: Effective Inspections
- [ ] Do you have checklists that focus reviewer attention on areas that have
    been problems in the past?
- [ ] Have you focused the inspection on defect detection rather than correction?
- [ ] Have you considered assigning perspectives or scenarios to help reviewers
    focus their preparation work?
- [ ] Are reviewersrs given enough time to prepare before the inspection meeting,
    and is each one prepared?
- [ ] Does each participant have a distinct role to play—moderator, reviewer, scribe, and so on?
- [ ] Does the meeting move at a productive rate?
- [ ] Is the meeting limited to two hours?
- [ ] Have all inspection participants received specific training in conducting
    inspections, and has the moderator received special training in moderation skills?
- [ ] Is data about error types collected at each inspection so that you can tailor
    future checklists to your organization?
- [ ] Is data about preparation and inspection rates collected so that you can
    optimize future preparation and inspections?
- [ ] Are the action items assigned at each inspection followed up,
    either personally by the moderator or with a reinspection?
- [ ] Does management understand that it should not attend inspection meetings?
- [ ] Is there a follow-up plan to assure that fixes are made correctly?

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

- **Developer tests tend to be “clean tests”** Developers tend to test for whether the code
    works (clean tests) rather than test for all the ways the code breaks (dirty tests).
- Developer testing tends to have an optimistic view of test coverage
- Developer testing tends to skip more sophisticated kinds of test coverage. A better coverage
    standard is to meet what’s called “100% branch coverage,” with every predicate term being tested
    for at least one true and one false value.

### 22.3 Bag of Testing Tricks 