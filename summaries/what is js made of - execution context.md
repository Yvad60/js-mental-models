# JavaScript mental models: What is JavaScript made of - the execution context

The execution context is like the environment in that a piece of JavaScript program will be running and for every line of code to be executed by the JavaScript engine there will have to be an execution context created.

There are 3 types of execution contexts:

- **The global execution context**: in this context, there will be all lines of code that are not enclosed in any function,
- **The function execution context**: this will only contain code that are specific to each function and every time the function is called (invoked) a whole brand new execution context will be created
- **The eval execution context**: this contains the code that is executed inside the “eval” function

There are two phases that happen in the execution context: the creation and the execution phaseg

In the creation phase, the engine will create the global object (window for browsers and global for Node) and assign “this” keyword accordingly. In this phase variables and functions will be hoisted, and variables will be assigned to undefined.

In the execution phase the engine will go over the code again and run all lines of code one by one.
