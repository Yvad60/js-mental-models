# JavaScript mental models: What is JavaScript made of: JS engine and runtime

JavaScript is a high-level, single-threaded, dynamic, and interpreted language which means it has a high level of abstraction (more readable), it can do one thing at a time (has a single thread), its variables can change types (dynamic), and it is run on the fly without compiling it beforehand.

For JavaScript to work we need the JS engine and the JS runtime. The JS engine is a computer program that parses and executes Js code, while the JS runtime is like a box (an environment) that contain everything required for the JS code to be completed, this will include the JS engine itself and other components depending on where JS is being run.

Browsers include a JavaScript runtime containing a JS engine and additional components like the Web API like DOM everything needed to run JavaScript on the client side. Node or Deno are JavaScript runtimes containing everything necessary to run Js code on the server.
