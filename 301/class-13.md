# CRUD

[Reading-notes](https://odehyazan.github.io/reading-notes/)

## Status Codes Based On REST Methods

### In your own words, describe what each group of status code represents

+ 100’s = Informational status codes
+ 200’s = The success codes
+ 300’s = Redirection codes
+ 400’s = The client error codes
+ 500’s = The server error codes

### What is a status code 202?

**Accepted - Often used for asynchronous processing. This code tells the client that the request was valid, but its processing will finish sometime in the future.**

### What is a status code 308?

**Permanent Redirect - This tells the client to use another URL to access the resource and not use the current URL anymore.**

### What code would you use if an update didn’t return data to a client?

**204 No Content.**

### What code would you use if a resource used to exist but no longer does?

**410 Gone.**

### What is the ‘Forbidden’ status code?

**403 Forbidden.**


[Build A REST API With Node.js, Express, & MongoDB - Quick - First 20 minutes](https://www.youtube.com/channel/UCFbNIlppjAuEX4znoulh0Cw)

### Why do we need to pull our MongoDB database string out of our server and put it into our .env?

**because we need it to work with others than our local host.**

### What is middleware?

**functions that has access to the HTTP request and response for each route (or path) it's attached to.**


### What does app.use(express.json()) do?

**Recognize the incoming Request Object as a JSON Object.**

### What does the /:id mean in a route?

**Passing Parameters to a Route.**

### What is the difference between PUT and PATCH?

**In a PUT request, the enclosed entity is considered to be a modified version of the resource stored on the origin server, and the client is requesting that the stored version be replaced.**<br>

**With PATCH, however, the enclosed entity contains a set of instructions describing how a resource currently residing on the origin server should be modified to produce a new version.**

### How do you make a default value in a schema?

**Your schemas can define default values for certain paths. If you create a new document without that path set, the default will kick in.**

**Note: Mongoose only applies a default if the value of the path is strictly undefined.**

### What does a 500 error status code mean?

**Internal Server Error.**

### What is the difference between a status 200 and a status 201?

**200 status code is by far the most common returned. It means, simply, that the request was received and understood and is being processed.**

**201 status code indicates that a request was successful and as a result, a resource has been created.**
