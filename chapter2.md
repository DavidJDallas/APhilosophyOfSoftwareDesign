## The Nature of Complexity

We should always be aiming for the simplest design. Complexity is defined as:

`Anything rerlated to the structure of a software system that makes it hard to understand and modify the system`

In a complex system, it takes a lot of work to implement even small improvements. In a simple system, larger improvements can be implemented with less effort. 

We can encapsulate complexity - 'Isolating complexity in a place where it will never be seen is almost as good as eliminating the complexity entirely'. 


### Symptoms of Complexity

(1) A seemingly simple change requires code modifications in many different places.

'One of the goals of good design is to reduce the amount of code that is affected by each design decision, so design changes don't require very many code modifications'. 

(2) Cognitive Load. Refers to how much a developer needs to know in order to complete a task. Can arise in many ways: APIs with many methods, global variables, inconsistencies, and dependencies between modules. 

A side note on global variables: global variables are risky to use because they are a shared state, and can be accessed by many different pieces of code which can mutate it. Something else could be changing the state that you're unaware of and the variable may be unsuitable when using it. There's an increased risk of it breaking/not working. 
We can counter global variables by using encapsulation and limited mutability. In OOP this means creating classes from which we can build objects that wrap around this state and provide controlled state mutation. In FP we get rid of state and pass immutable values around. 
Interestingly, Rust's borrow checker allows for shared immutables but doesn't allow for share mutables. 

Note also that sometimes an approach that requires more lines of code is actually simpler, because it reduces cognitive load. For instance, writing a function and setting well named variables along the way that adds 3 more lines, as opposed to simply returning a long single line of code with an implicit return. 

(3) Unknown unknowns: It is not obvious which pieces of code must be modified to complete a task, or what information a developer must have to carry out the task successfully. These are the worst manifestations of complexity. 

One of the most important goals of good design is for a system to be obvious. 

### Causes of Complexity

Complexity is cause by two things: Dependencies and obscurity. 

A dependency is defined as existing when a given piece of code can't be understood and modified in isolation; the code relates in some way to other code, and the other code must be considered and/or modified if the given code is changed. 

Dependencies are a fundamental part of software and can't be eliminated. However, one of the goals of software design is to reduce the number of dependencies and to make the dependencies as simple and obvious as possible. 

Obscurity occurs when important information isn't obvious. Examples include variable names that are so generic that they don't carry much useful info, or the documentation for a variable might not specify its units, or the documentation for a variable may not specify its units. Obscurity is often associated with dependencies, where it's not obvious that a dependency exists. 

In many cases, obscurity arises because of inadequate documentation. But it's also a design issue. If a system has a clean and obvious design, it needs less documentation. And the need for extensive documentation is often a red flag that the design isn't quite right. 

'Dependencies lead to change amplification and a high cognitive load. Obscruity creates unknown unknowns and also contributes to cognitive load. 

Complexity is also incremental and typically occurs through many many small increments. 
