# In memory storage

[Reading-notes](https://odehyazan.github.io/reading-notes/)

## Understanding the JavaScript Call Stack

### What is a ‘call’?

**The call stack is primarily used for function invocation (call) and call stack is a data structure that uses the Last In, First Out (LIFO) principle to temporarily store and manage function invocation (call).**

### How many ‘calls’ can happen at once?

**ne at a time.**

### What does LIFO mean?

**Last In, First Out, it means that the last function that gets pushed into the stack is the first to be pop out, when the function returns.**

### Draw an example of a call stack and the functions that would need to be invoked to generate that call stack.

![call stack](https://res.cloudinary.com/practicaldev/image/fetch/s--PO9oUsFs--/c_imagga_scale,f_auto,fl_progressive,h_420,q_auto,w_1000/https://dev-to-uploads.s3.amazonaws.com/i/st73hnavf3vbeitow7ln.jpeg)


### What causes a stack overflow?

**A stack overflow occurs when there is a recursive function (a function that calls itself) without an exit point. The browser (hosting environment) has a maximum stack call that it can accomodate before throwing a stack error.**`

**Here is an example:**

**`function callMyself(){`**
  **`callMyself();`**
**`}`**

**`callMyself();`**

**The `callMyself()` will run until the browser throws a “Maximum call size exceeded”. And that is a stack overflow.**

## JavaScript error messages

### What is a ‘refrence error’?

**When you try to use a variable that is not yet declared you get this type os errors.**

### What is a ‘syntax error’?

**This occurs when you have something that cannot be parsed in terms of syntax.**

### What is a ‘range error’?

**When trying to pass a number as an argument to a function that does not allow a range that includes that number. This can be encountered when to create an array of an illegal length with the Array constructor, or when passing bad values to the numeric methods Number.**

### What is a ‘type error’?

**The TypeError object represents an error when an operation could not be performed, typically (but not exclusively) when a value is not of the expected type.**

**A TypeError may be thrown when:**

**1. An operand or argument passed to a function is incompatible with the type expected by that operator or function.**
**2. when attempting to modify a value that cannot be changed.**
**3. When attempting to use a value in an inappropriate way.**

### What is a breakpoint?

**In the debugger window, you can set breakpoints in the JavaScript code, at each breakpoint, JavaScript will stop executing, and let you examine JavaScript values.**

### What does the word ‘debugger’ do in your code?

**When the debugger is invoked, execution is paused at the debugger statement. It is like a breakpoint in the script source.**
