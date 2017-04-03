# Software Development Principles and Their Rationale

This repository is a reference for myself to remember common software development principles, and to understand why we would belive those principles.

## General Principles

General principles apply to both software design and implementation.

#### KISS - Keep it simple, stupid!

The KISS principle states that most systems work best if they are kept simple rather than made complicated; therefore simplicity should be a key goal in design and unnecessary complexity should be avoided.

Rationale:

* Takes less time to write.

* Has fewer bugs. There are two ways to write code: write code so simple there are obviously no bugs in it, or write code so complex that there are no obvious bugs in it.

* Is easier to modify by yourself or others.

#### Information hiding

Information hiding is the principle of segregation, of the design decisions in a computer program that are most likely to change, thus protecting other parts of the program from extensive modification if the design decision is changed.

The protection involves providing a stable interface which protects the remainder of the program from the implementation (the details that are most likely to change).

> Question: How to do know which are stable and which are unstable?

Similar principle:

* Encapsulation
* Hide implementation details
* Law of Demeter

Rationale:

* Ease of maintain. Protects the remainder of the program from the implementation of an unstable module.

#### Single responsibility principle

"A class should have only one reason to change."

Similar principles:

* Minimize coupling
* Maximize cohesion
* Separation of concerns

Rationale:

* Makes the class more robust. If we coupling two responsibility together, there is a greater danger that the other part will break if we change one.

## Design Level Principles

#### YAGNI - You aren't gonna need it

A programmer should not add functionality until deemed necessary.

It is meant to be used in combination with several other practices, such as continuous refactoring, continuous automated unit testing, and continuous integration. Used without continuous refactoring, it could lead to disorganized code and massive rework.

Similar principles:

* Do the simplest thing that could possibly work

Rationale:

* Save time. Avoid developing features that will not be used in the future.

#### Principle of least astonishment

"If a necessary feature has a high astonishment factor, it may be necessary to redesign the feature."

"People are part of the system. The design should match the user's experience, expectations, and mental models."

Rationale:

* Save time. Takes less time for the audience to understand and to make sense.

## Code Level Principles

#### DRY - Don't repeat yourself

"Every piece of knowledge must have a single, unambiguous, authoritative representation within a system".

The principle has been formulated by Andy Hunt and Dave Thomas in their book The *Pragmatic Programmer*. They apply it quite broadly to include "database schemas, test plans, the build system, even documentation."

Rationale:

* Save time. A modification of any single element of a system does not require a change in other logically unrelated elements.

* Elements that are logically related all change predictably and uniformly, and are thus kept in sync.

#### Avoid premature optimization

Don’t even think about optimization unless your code is working, but slower than you want. Only then should you start thinking about optimizing, and then only with the aid of empirical data.

"We should forget about small efficiencies, say about 97% of the time: premature optimization is the root of all evil"

Rationale:

* Optimization can reduce readability and add code that is used only to improve the performance. This may complicate programs or systems, making them harder to maintain and debug.

#### Don't make me think

Code should be easily read and understood with a minimum of effort required.

 "Always code as if the person who ends up maintaining your code is a violent psychopath who knows where you live."

Similar principles:

* Write code for the maintainer

Rationale:

* Save time. If we need to maintain the code in the future, it saves us time to understand where we were.
