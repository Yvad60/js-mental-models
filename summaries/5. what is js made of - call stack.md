# JavaScript mental models: What is JavaScript made of - call stack

The call stack is the mechanism of the engine to know the current location in a program with multiple function calls. The call stack is a stack data structure which means that the last function to be pushed (added) on the stack will be the first to be popped (removed) and functions will continue to be pushed and popped onto the stack until there is no more code to execute remaining.

```js
function first (){
  second()
  return "first"
}

const second(){
  third()
  return "second"
}

const third(){
  return "third"
}

first()
```

The above code includes 3 functions where the first function calls the second and the second calls the third. In this case, the first will be added to the stack first, and when the second will be called it will be pushed on the top, the same will apply to the third, and since the last third is the last when it finishes executing it will be popped from the stack, the second follows and the first will be the last to go
