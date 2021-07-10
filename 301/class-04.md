# React and Forms

[Reading-notes](https://odehyazan.github.io/reading-notes/)

## React Docs - Forms

### What is a ‘Controlled Component’?

**Combine the element with updates come from `setState()` by making the React state be the “single source of truth”. Then the React component that renders a form also controls what happens in that form on subsequent user input. An input form element whose value is controlled by React.**

### Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why.

**Since the value attribute is set on our form element, the displayed value will always be `this.state.value`, making the ***React state the source of truth***. Since handleChange runs on every keystroke to update the React state, the displayed value will update as the user types.**

### How do we target what the user is entering if we have an event handler on an input field?

**`event.target.name.value`**

## The Conditional (Ternary) Operator Explained

### Why would we use a ternary operator?

**Use the ternary operator to simplify your if-else statements that are used to assign values to variables. The ternary operator is commonly used when assigning post data or validating forms.**

### Rewrite 

**`x===y ? console.log(true) : console.log(false);`**