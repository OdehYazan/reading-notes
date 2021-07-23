# FUNCTIONAL PROGRAMMING

[Reading-notes](https://odehyazan.github.io/reading-notes/)

## What is functional programming?

**Functional programming is a programming paradigm — a style of building the structure and elements of computer programs — that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data.**

## What is a pure function and how do we know if something is a pure function?

**It returns the same result if given the same arguments (it is also referred as deterministic).**

## What are the benefits of a pure function?

**he code’s definitely easier to test. We don’t need to mock anything. So we can unit test pure functions with different contexts:**

1. Given a parameter A → expect the function to return value B

2. Given a parameter C → expect the function to return value D

## What is immutability?

**When data is immutable, its state cannot change after it’s created. If you want to change an immutable object, you can’t. Instead, you create a new object with the new value.**

## What is Referential transparency?

**Basically, if a function consistently yields the same result for the same input, it is referentially transparent.**

## What is a module?

**Module in Node. js is a simple or complex functionality organized in single or multiple JavaScript files which can be reused throughout the Node. js application. Each module in Node. js has its own context, so it cannot interfere with other modules or pollute global scope.**

## What does the word ‘require’ do?

**Used to load and cache JavaScript modules.**

## How do we bring another module into the file the we are working in?

**var arthmetic = require("arthmetic");**

## What do we have to do to make a module available?

**`module.exports= <module name>`**
