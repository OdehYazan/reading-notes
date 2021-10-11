[Reading-notes](https://odehyazan.github.io/reading-notes/)

# Spring RESTful Routing & Static Files

## Spring MVC: @RequestMapping

**Simply put, the annotation is used to map web requests to Spring Controller methods.**

### @RequestMapping Basics

**1. @RequestMapping — by Path.**

**`@RequestMapping(value = "/ex/foos", method = RequestMethod.GET)`**<br>
   **`@ResponseBody`**<br>
   **`public String getFoosBySimplePath() {`**<br>
    **`return "Get some Foos";`**<br>
**`}`**<br>

**2. @RequestMapping — the HTTP Method.**

 **The HTTP method parameter has no default. So, if we don't specify a value, it's going to map to any HTTP request.**

 **Here's a simple example, similar to the previous one, but this time mapped to an HTTP POST request:**

 **`@RequestMapping(value = "/ex/foos", method = POST)`**<br>
   **`@ResponseBody`**<br>
   **`public String postFoos() {`**<br>
    **`return "Post some Foos";`**<br>
**`}`**<br>

### RequestMapping and HTTP Headers

**1. @RequestMapping With the headers Attribute.**
**The mapping can be narrowed even further by specifying a header for the request:**

 **`@RequestMapping(value = "/ex/foos", headers = "key=val", method = GET)`**<br>
   **`@ResponseBody`**<br>
   **`public String getFoosWithHeader() {`**<br>
    **`return "Get some Foos with Header";`**<br>
**`}`**<br>

**and even multiple headers via the headers attribute of @RequestMapping:**

**`@RequestMapping(`**<br>
  **`value = "/ex/foos",`**<br>
  **`headers = { "key1=val1", "key2=val2" }, method = GET)`**<br>
   **`@ResponseBody`**<br>
**`public String getFoosWithHeaders() {`**<br>
   **`return "Get some Foos with Header";`**<br>
**`}`**
**2. @RequestMapping Consumes and Produces.**

### RequestMapping With Path Variables

**1.  Single @PathVariable.**
**2. Multiple @PathVariable.**

### Accessing Data with JPA

**1. Starting with Spring Initializr.**
**2. Define a Simple Entity.**
**3. Create Simple Queries**
**4. Create an Application Class.**
**5. Build an executable JAR**

## Baeldung: Comparing repositories

## Spring Data Repositories

**1. CrudRepository provides CRUD functions.**
**2. PagingAndSortingRepository provides methods to do pagination and sort records.**
**3. JpaRepository provides JPA related methods such as flushing the persistence context and delete records in a batch.**

### JpaRepository

**methods in brief:**

**1. findAll() – get a List of all available entities in database.**

**2. findAll(…) – get a List of all available entities and sort them using the provided condition.**

**3. save(…) – save an Iterable of entities. Here, we can pass multiple objects to save them in a batch.**

**4. flush() – flush all pending task to the database.**

**5. saveAndFlush(…) – save the entity and flush changes immediately.**

**6. deleteInBatch(…) – delete an Iterable of entities. Here, we can pass multiple objects to delete them in a batch.**

