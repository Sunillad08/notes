# HTTP
[Back to networking page](./index.md)

---

## What is HTTP?
**Hyper Text Transfer Protocol**
The Hypertext Transfer Protocol (HTTP) is an application layer protocol in the Internet protocol suite model for distributed, collaborative, hypermedia information systems. HTTP is the foundation of data communication for the World Wide Web, where hypertext documents include hyperlinks to other resources that the user can easily access, for example by a mouse click or by tapping the screen in a web browser.

Development of HTTP was initiated by Tim Berners-Lee at CERN in 1989. Development of early HTTP Requests for Comments (RFCs) was a coordinated effort by the Internet Engineering Task Force (IETF) and the World Wide Web Consortium (W3C), with work later moving to the IETF.

Runs on port 80. TCP is used.
Stateless protocol so cookies are used.

---

## Why HTTP is used?
HTTP is used to tranfer data which is in form of web pages and many more things.
Internet basically runs on HTTP protocol.

---

## URL 
Uniform Resource Locator i.e URL is way of specifying how , where and what information to get.

URL : **Method :// Host : Port / Path**

Example : ```http://www.w4.org/hypertext/www/project.html```

---

## Cookies
Cookies are used because http is stateless protocol. It can't identify the client. Cookies are simple information packets that can identify user. set-cookie is method used to create cookie. Cookies are controversial as they invade privacy.

---

## Web documents 
1. Static documents : Simple HTTP pages with information
2. Dynamic documents : Document created on server based on clients input or authentication. 
3. Active documents : This document will run of clients browser for example gif , animated graphics. Browser is responsible to manage and execute this files.

---

## Request methods

An HTTP/1.1 request made using telnet. The request message, response header section, and response body are highlighted.

The HTTP/1.0 specification defined the GET, HEAD and POST methods, and the HTTP/1.1 specification added five new methods: PUT, DELETE, CONNECT, OPTIONS, and TRACE. 

Method names are case sensitive This is in contrast to HTTP header field names which are case-insensitive.

- GET : The GET method requests that the target resource transfers a representation of its state. GET requests should only retrieve data and should have no other effect. 
- HEAD : The HEAD method requests that the target resource transfers a representation of its state, like for a GET request, but without the representation data enclosed in the response body. This is useful for retrieving the representation metadata in the response header, without having to transfer the entire representation.
- POST : The POST method requests that the target resource processes the representation enclosed in the request according to the semantics of the target resource. For example, it is used for posting a message to an Internet forum, subscribing to a mailing list, or completing an online shopping transaction.
- PUT : The PUT method requests that the target resource creates or updates its state with the state defined by the representation enclosed in the request.
- DELETE : 	The DELETE method requests that the target resource deletes its state.
- CONNECT : The CONNECT method request that the intermediary establishes a TCP/IP tunnel to the origin server identified by the request target. It is often used to secure connections through one or more HTTP proxies with TLS.
- OPTIONS : The OPTIONS method requests that the target resource transfers the HTTP methods that it supports. This can be used to check the functionality of a web server by requesting '\*' instead of a specific resource.
- TRACE : The TRACE method requests that the target resource transfers the received request in the response body. That way a client can see what (if any) changes or additions have been made by intermediaries.
- PATCH : 	The PATCH method requests that the target resource modifies its state according to the partial update defined in the representation enclosed in the request.
	
All general-purpose HTTP servers are required to implement at least the GET and HEAD methods, and all other methods are considered optional by the specification.

![http](https://media.geeksforgeeks.org/wp-content/uploads/20191025104128/1041.png)

---

## Status code
A basic breakdown of the status codes is:

100-199: Information
200-299: Successes (200 OK is the "normal" response for a GET)
300-399: Redirects (the information you want is elsewhere)
400-499: Client errors (You did something wrong, like asking for something that doesn't exist)
500-599: Server errors (The server tried, but something went wrong on their side)

Check more detailed status code [here](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status) ....

---

## HTTP versions
- HTTP/1.0 (1996)  
- HTTP/1.1 (1997)  
- HTTP/1.1 (1999)  
- HTTP/1.1: Message Syntax and Routing (2014)  
- HTTP/1.1: Semantics and Content (2014)  
- HTTP/1.1: Conditional Requests (2014)  
- HTTP/1.1: Range Requests (2014)  
- HTTP/1.1: Caching (2014)  
- HTTP/1.1: Authentication (2014)  
- HTTP/2 (2015)  
- HTTP/2: HPACK Header Compression (2015)

---

## HTTP Problem
- Because HTTP transfers data in Plain text and that is security issue. That's why [HTTPS](HTTPS.md) is used.

---

### Sources :
- [Wiki](https://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol)
- [Detailed Youtube video](https://youtu.be/0OrmKCB0UrQ)