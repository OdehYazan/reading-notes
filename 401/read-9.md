[Reading-notes](https://odehyazan.github.io/reading-notes/)

# WRRC and Java

## Review: High-level HTTP

**1. Local Processing**

**Depending on how in depth you want to get, much can happen during this step depending on the application making the request. I am going to proceed on the understanding this request is being made by a browser, as opposed to cURL, an API client like Postman, or some other app.**

**your browser extracts the "scheme"/protocol (we have established that this will be HTTP), host (www.example.com),and optional port number, resource path, and query strings that are specified in the form.**

**example is `|http|://|www.example.com||:5000||/mainpage||?query=param&query2=param2|`**

 **Now that the browser has the intended hostname for the request, it needs to resolve an IP address1. The browser will then look through its own cache of recently requested URLs, the operating system’s cache of recent queries, your router’s cache, and your DNS cache.**

**Resolve an IP:**

**If the cache lookup fails (we will assume it does), your browser fires off a DNS request using UDP3. The DNS request contains the pre configured IP for your DNS server and your return IP in its header. The hostname for which you are trying to resolve an IP is in the request’s "Question" section. UDP is a lightweight protocol, but the tradeoff is that it offers no guarantees in terms of delivery, and there is no acknowledgement other than a response being sent and received.**

**Your request will now have to travel many network devices to reach its target DNS server. Whenever the packet hits a piece of networking equipment, the device uses a routing table to determine which other device it is connected to that is most likely situated along the shortest path to the destination.**

**Once your request arrives at your configured DNS server, the server looks for the address associated with the requested hostname. If it finds one, it sends a response. If, on the other hand, the DNS server you have targeted cannot locate the given hostname, it passes the request along to another DNS server it is configured to defer to. This happens recursively until the address is found, or an "authoritative" nameserver is hit. If an address for the given domain cannot be resolved, the server responds with a failure and your browser returns an error.**

**We will assume the request is successful though, given that all of this is still a precursor. If the response makes it back (remember, with UDP there’s no guarantee!), the requesting client now has a target IP. It will also have received a piece of information as part of the answer that will let it know how long the returned answer can be cached for.**


**Establish a TCP Connection:**

**To establish a connection, TCP uses a three-way handshake. Before a client attempts to connect with a server, the server must first bind to and listen at a port to open it up for connections: this is called a passive open. Once the passive open is established, a client may initiate an active open.**

**Send an HTTP Request:**

**Send HTTP Request is an asynchronous activity that sends an HTTP request and waits for a response from the web server. This activity sends a request to a server that is compliant with either the HTTP 1.1 or 1.0 specification.**

**Tearing Down and Cleaning Up:**

**1. Once the response has been fully delivered, the client sends a FIN packet at the TCP level, to which the server responds with an ACK, and then generally sends a FIN of its own, which the client responds to with its own ACK signal. The client then waits for a brief timeout, during which it cannot accept new connections, to prevent delayed packets from previous connections arriving during subsequent activities on the port. This four way handshake12 signals the end of the TCP connection.**

**2. At this point, your browser begins processing what it has received. If it is an image, data, or other media file that is being consumed by some application inside the browser, a variety of things can happen. If the data received is HTML, the browser will start parsing the HTML, and rendering the page you requested. As it parses, the browser may come across links to images or other media that are external to the HTML it has received, and will spin up new requests for that content, restarting this whole process (although usually skipping steps 1 & 2 thanks to caching). But, given that we were only interested in the lifecycle of an individual request: our (application’s) work is done, congratulations!**

## Java HTTP Request example

### Overview

**Starting with JDK 11, Java provides a new API for performing HTTP requests, which is meant as a replacement for the HttpUrlConnection, the HttpClient API.**

### HttpUrlConnection

**The HttpUrlConnection class allows us to perform basic HTTP requests without the use of any additional libraries. All the classes that we need are part of the java.net package.**

**The disadvantages of using this method are that the code can be more cumbersome than other HTTP libraries and that it does not provide more advanced functionalities such as dedicated methods for adding headers or authentication.**

### Creating a Request

**We can create an HttpUrlConnection instance using the openConnection() method of the URL class. Note that this method only creates a connection object but doesn't establish the connection yet.**

**The HttpUrlConnection class is used for all types of requests by setting the requestMethod attribute to one of the values: GET, POST, HEAD, OPTIONS, PUT, DELETE, TRACE.**

### Adding Request Parameters

**If we want to add parameters to a request, we have to set the doOutput property to true, then write a String of the form param1=value¶m2=value to the OutputStream of the HttpUrlConnection.**

**To facilitate the transformation of the parameter Map, we have written a utility class called ParameterStringBuilder containing a static method, getParamsString(), that transforms a Map into a String of the required format.**

### Setting Request Headers

**Adding headers to a request can be achieved by using the setRequestProperty() method.**

**To read the value of a header from a connection, we can use the getHeaderField() method.**

### Configuring Timeouts

**HttpUrlConnection class allows setting the connect and read timeouts. These values define the interval of time to wait for the connection to the server to be established or data to be available for reading.**

**To set the timeout values, we can use the setConnectTimeout() and setReadTimeout() methods.**

### Handling Cookies

**The java.net package contains classes that ease working with cookies such as CookieManager and HttpCookie.**
**First, to read the cookies from a response, we can retrieve the value of the Set-Cookie header and parse it to a list of HttpCookie objects.**
**Next, we will add the cookies to the cookie store**
**Finally, to add the cookies to the request, we need to set the Cookie header, after closing and reopening the connection**

### Handling Redirects

**We can enable or disable automatically following redirects for a specific connection by using the setInstanceFollowRedirects() method with true or false parameter.**
**It is also possible to enable or disable automatic redirect for all connections**
**By default, the behavior is enabled.**

### Reading the Response

**Reading the response of the request can be done by parsing the InputStream of the HttpUrlConnection instance.**

**To execute the request, we can use the getResponseCode(), connect(), getInputStream() or getOutputStream() methods.**

**To close the connection, we can use the disconnect() method.**

### Reading the Response on Failed Requests

**f the request fails, trying to read the InputStream of the HttpUrlConnection instance won't work. Instead, we can consume the stream provided by HttpUrlConnection.getErrorStream().**

