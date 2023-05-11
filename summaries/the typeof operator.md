# Javascript mental model: the typeof operator

The type of operator is a unary operator (takes only one operand) and returns a string of its data type. JavaScript by default recognizes 8 data types: number, string, boolean, bigInt, symbols, undefined, null and objects, but not every time the typeof operator returns the correct data type according to the ECMAScript specification

**typeof null will return “object”**: this doesn’t mean that null is an object in JS, null is a data type itself and the reason it returns an object was a bug that was created in the first version of JS and too many existing websites have taken advantage of that behavior to change it and it was left that way.

**Typeof function will return “function”**: even if functions are data type of object because The ECMAScript specification considers functions as special kind of objects because they can be callable but everything and that’s why the operator will return “function”, every other kind of object will return “object”
