# Readings: REST

[Reading-notes](https://odehyazan.github.io/reading-notes/)

## What Google Learned From Its Quest to Build the Perfect Team

[What Google Learned About Teams](https://odehyazan.github.io/reading-notes/201/class-14b)

**They conducted hundreds of double-blind interviews with leaders to get a sense of what they thought drove team effectiveness. The researchers then looked at existing survey data, including over 250 items from the annual employee engagement survey and gDNA, Google’s longitudinal study on work and life, to see what variables might be related to effectiveness. Here are some sample items used in the study that participants were asked to agree or disagree with.**

- **Group dynamics: I feel safe expressing divergent opinions to the team.**

- **Skill sets: I am good at navigating roadblocks and barriers.**

- **Personality traits: I see myself as someone who is a reliable worker**

- **Emotional intelligence: I am not interested in other people’s problems**

### Who is Roy Fielding?

**Roy Thomas Fielding (born 1965) is an American computer scientist, one of the principal authors of the HTTP specification and the originator of the Representational State Transfer (REST) architectural style. He is an authority on computer network architecture and co-founded the Apache HTTP Server project.**

### Why don’t the techniques that we use today work well when we need to be able to talk to all of the machines in the world?

 **Because they weren't designed to be used like that. When Fielding and his colleagues started building the web, being able to talk to any machine anywhere in the world was a primary concern. But most of the techniques developers later used to get computers to talk to each other didn't have those requirements. You just needed to talk to a small group of machines.**

### What is the HTTP protocol that Fielding and his friends created?

**The Hypertext Transfer Protocol (HTTP) is a protocol which allows the fetching of resources, such as HTML documents. It is the foundation of any data exchange on the Web and it is a client-server protocol, which means requests are initiated by the recipient, usually the Web browser. A complete document is reconstructed from the different sub-documents fetched, for instance text, layout description, images, videos, scripts, and more.**
[MDN](https://developer.mozilla.org/en-US/docs/Web/HTTP/Overview)
![http](https://developer.mozilla.org/en-US/docs/Web/HTTP/Overview/fetching_a_page.png)

### HTTP request methods

**GET,POST,PUT and PATCH these what we will explain.**

### What does a GET do?

**GET is used to retrieve and request data from a specified resource in a server. GET is one of the most popular HTTP request techniques. In simple words, the GET method is used to retrieve whatever information is identified by the Request-URL.**

### What does a POST do?

**In computing, POST is a request method supported by HTTP used by the World Wide Web. By design, the POST request method requests that a web server accepts the data enclosed in the body of the request message, most likely for storing it. It is often used when uploading a file or when submitting a completed web form in other words POST is used to send data to a server to create/update a resource.**

### What does PUT do?

**A PUT is used to update existing data at a given URL, or to create something new when you know what the URI is going to be and it doesn't already exist (as opposed to a POST which will create something and return a URL to it if necessary).**

### What does PATCH do?

**PATCH method is a request method supported by the Hypertext Transfer Protocol (HTTP) protocol for making partial changes to an existing resource. The PATCH method provides an entity containing a list of changes to be applied to the resource requested using the HTTP Uniform Resource Identifier (URI).**


