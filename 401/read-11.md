[Reading-notes](https://odehyazan.github.io/reading-notes/)

# Spring

**The Spring Framework is an application framework and inversion of control container for the Java platform. The framework's core features can be used by any Java application, but there are extensions for building web applications on top of the Java EE platform.**

**Spring MVC:**

**The Spring Web model-view-controller (MVC) framework is designed around a Dispatcher Servant that dispatches requests to handlers, with configurable handler mappings, view resolution, locale and theme resolution as well as support for uploading files.**

## What You Will Build

**You will build an application that has a static home page and that will also accept HTTP GET requests at: `http://localhost:8080/greeting`.**

**It will respond with a web page that displays HTML. The body of the HTML will contain a greeting: “Hello, World!”.**

**You can customize the greeting with an optional `name` parameter in the query string. The URL might then be `http://localhost:8080/greeting?name=User`.**

**The `name` parameter value overrides the default value of World and is reflected in the response by the content changing to “Hello, User!”**

## Spring Initializr

**The Spring Initializer is ultimately a web application that can generate a Spring Boot project structure for you. ... It doesn't generate any application code, but it will give you a basic project structure and either a Maven or a Gradle build specification to build your code with.**

## Web API Controller

**Web API Controller is similar to ASP.NET MVC controller. It handles incoming HTTP requests and send response back to the caller. Web API controller is a class which can be created under the Controllers folder or any other folder under your project's root folder.**

## Spring Boot Devtools

**The spring-boot-devtools module includes an embedded LiveReload server that can be used to trigger a browser refresh when a resource is changed. LiveReload browser extensions are freely available for Chrome, Firefox and Safari from livereload.com.**

# Spring MVC and Thymeleaf

## Spring model attributes

**Spring MVC calls the pieces of data that can be accessed during the execution of views model attributes. The equivalent term in Thymeleaf language is context variables.**

***There are several ways of adding model attributes to a view in Spring MVC:***

**1.addAttribute.**
**2. ModelAndView.**
**3. @ModelAttribute.**

## Request parameters

**In Spring MVC, the @RequestParam annotation is used to read the form data and bind it automatically to the parameter present in the provided method. Including form data, it also maps the request parameter to query parameter and parts in multipart requests.**

## Session attributes

**SessionAttribute annotation is the simplest and straight forward instead of getting session from request object and setting attribute. Any object can be added to the model in controller and it will stored in session if its name matches with the argument in @SessionAttributes annotation.**

## ServletContext attributes

**The ServletContext attributes are shared between requests and sessions. In order to access ServletContext attributes in Thymeleaf you can use the #servletContext.**

## Spring beans

**Spring beans are the objects which are created and managed completely by spring container. These beans are the heart of the application. Beans can be defined in spring either by using XML configuration or by using Annotation. In XML configuration, bean can be defined using < bean > tag inside < beans > tag.**


