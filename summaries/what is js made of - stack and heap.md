# JavaScript mental models: What is JavaScript made of - Heap and Stack memory

Internally in the JavaScript runtime data is stored either in the stack or the heap depending on the datum type to store. General primitive values since their memory allocation is fixed are stored in the stack while objects like arrays, objects, or functions are as their memory allocation can change they are stored in the Heap
Taking example

```js
const name = "John" // on the stack 
const age = 10  // on the stack 
const address = { // on the heap
  country: "Rwanda",
  city: "Kigali"
}
```

Values like name and age are stored on the stack, while the address which is an object is allocated memory in the Heap
When an object is allocated memory in the stack a reference to that object is stored in the stack and from then the reference is used to mention that object when the reference is mentioned the real object is retrieved from the heap

The above implementation is not always the case it may vary in different JavaScript runtimes according to the desired memory optimization
