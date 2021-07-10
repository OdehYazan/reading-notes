# Putting it all together

[Reading-notes](https://odehyazan.github.io/reading-notes/)

## Thinking in React
![thinking](https://res.cloudinary.com/practicaldev/image/fetch/s--FgvCNIB1--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://thepracticaldev.s3.amazonaws.com/i/40ealcr41k0wtg9sy19x.png)

### How would you break a mock into a component hierarchy?

**The first thing you’ll want to do is to draw boxes around every component (and sub component) in the mock and give them all names.**

### What is the `single responsibility principle` and how does it apply to components?

**The single-responsibility principle (SRP) is a computer-programming principle that states that every module, class or function in a computer program should have responsibility over a single part of that program's functionality, and it should encapsulate that part. All of that module, class or function's services should be narrowly aligned with that responsibility.**

### What does it mean to build a ‘static’ version of your application?

**To build a static version of your app that renders your data model, you’ll want to build components that reuse other components and pass data using props. props are a way of passing data from parent to child. If you’re familiar with the concept of state, don’t use state at all to build this static version. State is reserved only for interactivity, that is, data that changes over time. Since this is a static version of the app, you don’t need it.**

### Once you have a static application, what do you need to add?

**Interactivity.**

### What are the three questions you can ask to determine if something is state?

1. **Is it passed in from a parent via props? If so, it probably isn’t state.**
2. **Does it remain unchanged over time? If so, it probably isn’t state.**
3. **Can you compute it based on any other state or props in your component? If so, it isn’t state.**

### How can you identify where state needs to live?

1. **Identify every component that renders something based on that state.**
2. **Find a common owner component (a single component above all the components that need the state in the hierarchy).**
3. **Either the common owner or another component higher up in the hierarchy should own the state.**
4. **If you can’t find a component where it makes sense to own the state, create a new component solely for holding the state and add it somewhere in the hierarchy above the common owner component.**