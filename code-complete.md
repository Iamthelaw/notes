# Code complete notes

## Chapter 3 Measure Twice, Cut Once: Upstream Prerequisites

### 3.1 Importance of Prerequisites

#### Do Prerequisites Apply to Modern Software Projects?

By far the most common project risks in software development are poor requirements and poor project planning, thus preparation tends to
focus on improving requirements and project plans.

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
- [ ] Are all the inputs to the system specified, including their source, accuracy, range of values, and frequency?
- [ ] Are all the outputs from the system specified, including their destination, accuracy, range of values, frequency, and format?
- [ ] Are all output formats specified for Web pages, reports, and so on?
- [ ] Are all the external hardware and software interfaces specified?
- [ ] Are all the external communication interfaces specified, including handshaking, error-checking, and communication protocols?
- [ ] Are all the tasks the user wants to perform specified?
- [ ] Is the data used in each task and the data resulting from each task specified?

##### Specific Nonfunctional (Quality) Requirements
- [ ] Is the expected response time, from the user’s point of view, specified for all necessary operations?
- [ ] Are other timing considerations specified, such as processing time, datatransfer rate, and system throughput?
- [ ] Is the level of security specified?
- [ ] Is the reliability specified, including the consequences of software failure, the vital information that needs to be protected from failure, and the strategy for error detection and recovery?
- [ ] Are minimum machine memory and free disk space specified?
- [ ] Is the maintainability of the system specified, including its ability to adapt to changes in specific functionality, changes in the operating environment, and changes in its interfaces with other software?
- [ ] Is the definition of success included? Of failure?

##### Requirements Quality
- [ ] Are the requirements written in the user’s language? Do the users think so?
- [ ] Does each requirement avoid conflicts with other requirements?
- [ ] Are acceptable tradeoffs between competing attributes specified—for example, between robustness and correctness?
- [ ] Do the requirements avoid specifying the design?
- [ ] Are the requirements at a fairly consistent level of detail? Should any requirement be specified in more detail? Should any requirement be specified in less detail?
- [ ] Are the requirements clear enough to be turned over to an independent group for construction and still be understood? Do the developers think so?
- [ ] Is each item relevant to the problem and its solution? Can each item be traced to its origin in the problem environment?
- [ ] Is each requirement testable? Will it be possible for independent testing to determine whether each requirement has been satisfied?
- [ ] Are all possible changes to the requirements specified, including the likelihood of each change?

##### Requirements Completeness
- [ ] Where information isn’t available before development begins, are the areas of incompleteness specified?
- [ ] Are the requirements complete in the sense that if the product satisfies every requirement, it will be acceptable?
- [ ] Are you comfortable with all the requirements? Have you eliminated requirements that are impossible to implement and included just to appease your customer or your boss

### 3.5 Architecture Prerequisite

#### Program Organization

In the architecture, you should find evidence that alternatives to the final organization
were considered and find the reasons for choosing the final organization over its alternatives. It’s frustrating to work on a class when it seems as if the class’s role in the system
has not been clearly conceived.

Each building block is a class, or it’s a collection of classes or routines that work together on high-level functions such as interacting with the user, displaying Web pages, interpreting commands, encapsulating
business rules, or accessing data. Every feature listed in the requirements should be
covered by at least one building block.

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
- [ ] Is the overall organization of the program clear, including a good architectural overview and justification?
- [ ] Are major building blocks well defined, including their areas of responsibility and their interfaces to other building blocks?
- [ ] Are all the functions listed in the requirements covered sensibly, by neither too many nor too few building blocks?
- [ ] Are the most critical classes described and justified?
- [ ] Is the data design described and justified?
- [ ] Is the database organization and content specified?
- [ ] Are all key business rules identified and their impact on the system described?
- [ ] Is a strategy for the user interface design described?
- [ ] Is the user interface modularized so that changes in it won’t affect the rest of the program?
- [ ] Is a strategy for handling I/O described and justified?
- [ ] Are resource-use estimates and a strategy for resource management described and justified for scarce resources like threads, database connections, handles, network bandwidth, and so on?
- [ ] Are the architecture’s security requirements described?
- [ ] Does the architecture set space and speed budgets for each class, subsystem, or functionality area?
- [ ] Does the architecture describe how scalability will be achieved?
- [ ] Does the architecture address interoperability?
- [ ] Is a strategy for internationalization/localization described?
- [ ] Is a coherent error-handling strategy provided?
- [ ] Is the approach to fault tolerance defined (if any is needed)?
- [ ] Has technical feasibility of all parts of the system been established?
- [ ] Is an approach to overengineering specified?
- [ ] Are necessary buy-vs.-build decisions included?
- [ ] Does the architecture describe how reused code will be made to conform to other architectural objectives?
- [ ] Is the architecture designed to accommodate likely changes?

##### General Architectural Quality
- [ ] Does the architecture account for all the requirements?
- [ ] Is any part overarchitected or underarchitected? Are expectations in this area set out explicitly?
- [ ] Does the whole architecture hang together conceptually?
- [ ] Is the top-level design independent of the machine and language that will be used to implement it?
- [ ] Are the motivations for all major decisions provided?
- [ ] Are you, as a programmer who will implement the system, comfortable with the architecture?

### 3.6 Amount of Time to Spend on Upstream Prerequisites

Generally, a well-run project devotes about 10 to 20 percent of its effort and about 20 to 30 percent of
its schedule to requirements, architecture, and up-front planning (McConnell 1998, Kruchten 2000).

>  If necessary, plan the architecture work as a separate project, too.
