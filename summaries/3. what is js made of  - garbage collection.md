# JavaScript mental models: What is JavaScript made of - Garbage collection

When a program runs it uses some memory on the machine to store variables and functions needed for it to run. To avoid overflowing our memory with program data memory for some variables or objects that are no longer needed has to be released and this is the main task of the garbage collector

The garbage collector finds objects that are no longer needed (known as garbage) and removes them to free up memory. The issue most of the time is to know that the memory is no longer needed so that it can be cleared and for this several algorithms are used to identify it

Reference counting garbage collection (anti-pattern): this way uses the algorithm of identifying that the object is no longer needed by checking it is not referenced by any object but this will not work for some cases as mentioned below

```js
const son = { name: "Tim" }; // the object is allocated memory
const dad = { name: "Steve" }; // the object is allocated memory
son.dad = dad; // son is now referencing dad
dad.son = son; // dad is now referencing son
son = null; //The son object still has dad ad references but its value is overwritten so there is no way to access dad in the code
dad = null; // same here
```

In this example with the reference counting garbage collection will not remove both of them even though there is no way to access them in the code.

Mark and sweep garbage collection: this is the new (implemented in modern browsers) garbage collection where an object is cleared when it can no longer be reached from the main object (window in browsers and global object in node).
In the above example, the son and dad objects will both be removed since they can no longer be accessed in code.
Global variables will not be cleared since they will always be accessed in the global object
