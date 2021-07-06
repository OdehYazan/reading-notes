# APIs

[Reading-notes](https://odehyazan.github.io/reading-notes/)

## What does REST stand for?

**Representational State Transfer.**

## What REST APIs are designed around ?

**REST APIs are designed around resources, which are any kind of object, data, or service that can be accessed by the client.**

## What is an identifer of a resource? Give an example

**which is a URI that uniquely identifies that resource. For example, the URI for a particular customer order might be:`https://adventure-works.com/orders/1`.**

## What are the most common HTTP verbs?

**The primary or most-commonly-used HTTP verbs (or methods, as they are properly called) are POST, GET, PUT, PATCH, and DELETE.**

## What should the URIs be based on?

**URIs should be based on nouns (the resource) and not verbs (the operations on the resource).**

## Give an example of a good URI:

**`https://adventure-works.com/orders // Good`**

**`https://adventure-works.com/create-order // Avoid this`**

## What does it mean to have a ‘chatty’ web API? Is this a good or a bad thing?

**avoid "chatty" web APIs that expose a large number of small resources. Such an API may require a client application to send multiple requests to find all of the data that it requires. Instead, you might want to denormalize the data and combine related information into bigger resources that can be retrieved with a single request.**

## What status code does a successful GET request return?

**A successful GET method typically returns HTTP status code 200 (OK).**

## What status code does an unsuccessful GET request return?

**It should return HTTP status code 406 (Not Acceptable).**

## What status code does a successful POST request return?

**It returns HTTP status code 201 (Created).**

## What status code does a successful DELETE request return?

**Respond with HTTP status code 204.**