# Passing Functions as Props

[Reading-notes](https://odehyazan.github.io/reading-notes/)

## React Docs - lists and keys

**What does .map() return?<br>map return the results of calling a provided function on every element in the calling array with the same array length.**

**If I want to loop through an array and display each value in JSX, how do I do that in React?<br>we use `map()`or `forEach()`.**

### Each list item needs a unique key

### What is the purpose of a key?

**Keys help React identify which items have changed, are added, or are removed. Keys should be given to the elements inside the array to give the elements a stable identity.**

## The Spread Operator

### What is the spread operator?

**Spread syntax refers to the use of an ellipsis of three dots `(…)` to expand an iterable object into the list of arguments.**

### List 4 things that the spread operator can do

+ **Copying an array**
+ **Concatenating or combining arrays**
+ **Using Math functions**
+ **Using an array as arguments**

### Give an example of using the spread operator to combine two arrays

1. **`const arr1 = [1,2,3]`**
2. **`const arr2 = [4,5,6]`**
3. **`const arr3 = [...arr1, ...arr2] //arr3 ==> [1,2,3,4,5,6]`**
=================================================================

+ **`const a = ['to', 'code'];`**
+ **`const b = ['learning', ...a, 'is', 'fun'];`**
+ **`// ['learning', 'to', 'code', 'is', 'fun']`**

### Give an example of using the spread operator to add a new item to an array

+ **`const fewFruit = ['🍏','🍊','🍌']`**
+ **`const fewMoreFruit = ['🍉', '🍍', ...fewFruit]`**
+ **`console.log(fewMoreFruit) //  Array(5) [ "🍉", "🍍", "🍏", "🍊", "🍌" ]`**

### Give an example of using the spread operator to combine two objects into one

1. **`const objectOne = {hello: "🤪"}`**
2. **`const objectTwo = {world: "🐻"}`**
3. **`const objectThree = {...objectOne, ...objectTwo, laugh: "😂"}`**
4. **`console.log(objectThree) // Object { hello: "🤪", world: "🐻", laugh: "😂" }`**
5. **`const objectFour = {...objectOne, ...objectTwo, laugh: () => {console.log("😂".repeat(5))}}`**
6. **`objectFour.laugh() // 😂😂😂😂😂`**

## How to Pass Functions Between Components

[Video](https://www.youtube.com/watch?v=c05OL7XbwXU)

### In the video, what is the first step that the developer does to pass functions between components?

**Create increment function where the states while change in the parent .js then send it to person object like props.**

### In your own words, what does the increment function do?

**Increase the count for each person in the class people when press the button.**

### How can you pass a method from a parent component into a child component?

**like props. `var={this.function}`**

### How does the child component invoke a method that was passed to it from a parent component?

**like any other props `{this.props.var}` var is the variable name in the parent which equals the function.**