---
layout: default
title: API Testing
parent: Knowledge
nav_order: 9
---

{: .no_toc }

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
- TOC
{:toc}
</details>

## HTTP methods

HTTP methods are standardized commands or actions that clients (e.g., web browsers, mobile apps) use to communicate with web servers. Each HTTP method defines a specific operation to be performed on a resource identified by a URL (Uniform Resource Locator). HTTP methods are an essential part of the HTTP protocol, which is the foundation of the World Wide Web.

Here are some commonly used HTTP methods:

1. **GET:** The GET method is used to request data from a specified resource. It retrieves data from the server without modifying the resource. GET requests are typically used for retrieving web pages, images, files, and other resources.

2. **POST:** The POST method is used to submit data to be processed to a specified resource. It sends data in the request body, often used for creating new resources, submitting forms, or sending data to a server to be processed.

3. **PUT:** The PUT method is used to update a resource or create a new resource if it does not exist at the specified URL. It replaces the entire resource with the new data provided in the request body.

4. **PATCH:** The PATCH method is similar to PUT but is used to make partial updates to a resource. It updates only the fields specified in the request body, leaving other fields unchanged.

5. **DELETE:** The DELETE method is used to request the removal of a resource from the server. It deletes the resource at the specified URL.

6. **HEAD:** The HEAD method is similar to GET but retrieves only the headers of the response, not the actual data content. It is often used to check the status and metadata of a resource without downloading the entire resource.

7. **OPTIONS:** The OPTIONS method is used to retrieve information about the communication options available for the target resource. It can provide details about supported HTTP methods, headers, and other communication parameters.

## HTTP status codes

HTTP status codes are three-digit numbers returned by a web server in response to a client's request made to the server over the HTTP protocol (Hypertext Transfer Protocol). These status codes are included in the response headers and serve as a way for the server to communicate the result of the request to the client's web browser or application. HTTP status codes are grouped into five classes, each with its own meaning:

1. **Informational (1xx):** These status codes indicate that the server has received the request and is continuing to process it. The client should continue to wait for a final response.

   - **100 (Continue):** The server has received the initial part of the request, and the client can continue to send the rest of the request.

2. **Successful (2xx):** These status codes indicate that the request was received, understood, and processed successfully.

   - **200 (OK):** The request was successful, and the server returns the requested data.
   - **201 (Created):** The request resulted in the creation of a new resource.
   - **204 (No Content):** The server successfully processed the request, but there is no additional information to send back.

3. **Redirection (3xx):** These status codes indicate that further action is needed by the client to complete the request. They are often used for URL redirection.

   - **301 (Moved Permanently):** The requested resource has been permanently moved to a new URL.
   - **302 (Found):** The requested resource has been temporarily moved to a different URL.
   - **304 (Not Modified):** The client's cached version of the resource is up to date, and no data is sent in the response.

4. **Client Error (4xx):** These status codes indicate that the client made an error or provided incorrect information in the request.

   - **400 (Bad Request):** The request was malformed or invalid.
   - **401 (Unauthorized):** Authentication is required, and the client has not provided valid credentials.
   - **403 (Forbidden):** The server understood the request but refuses to fulfill it.
   - **404 (Not Found):** The requested resource could not be found on the server.

5. **Server Error (5xx):** These status codes indicate that the server encountered an error while processing the request.

   - **500 (Internal Server Error):** A generic server error occurred, and the server cannot provide more specific information.
   - **502 (Bad Gateway):** The server, while acting as a gateway or proxy, received an invalid response from an upstream server.
   - **503 (Service Unavailable):** The server is currently unable to handle the request, typically due to overloading or maintenance.

HTTP status codes are an important part of the HTTP protocol and are used by web applications and browsers to understand the outcome of a request, enabling appropriate actions or responses. They are crucial for diagnosing and debugging issues in web communication.

## RESTful APIs

**Representational State Transfer (REST)** is an architectural style for designing and developing networked applications. It was first proposed by Roy Fielding in his 2000 doctoral dissertation, and it has since become the most widely used approach for building web APIs.

**Key Principles of REST**

1. **Client-server architecture:** Clients and servers are separate components that communicate through a well-defined interface.

2. **Statelessness:** Each request from a client to a server must contain all the information necessary to complete the request. The server does not store any client-specific information between requests.

3. **Cacheability:** Both clients and servers can cache responses to improve performance.

4. **Uniform interface:** Clients interact with resources using a consistent set of operations, such as GET, POST, PUT, and DELETE.

5. **Layered system:** Components can be layered on top of each other to provide additional functionality, such as security or load balancing.

6. **Code on demand (optional):** Clients can download and execute code from the server to extend their functionality.

**RESTful APIs and HTTP Methods**

RESTful APIs use HTTP methods to perform operations on resources. 

**URL Structure in RESTful APIs**

URLs in RESTful APIs are used to identify resources. The URL structure should be consistent and easy to understand. For example, the URL `/users/1` could be used to identify the user with the ID 1.

**Benefits of RESTful APIs**

* **Simple and easy to understand:** The principles of REST are straightforward, and the use of HTTP methods and URLs is familiar to many developers.

* **Flexible:** REST can accommodate a wide range of applications, from simple data retrieval to complex e-commerce systems.

* **Scalable:** RESTful APIs can handle a large number of concurrent users and requests.

* **Interoperable:** RESTful APIs can easily interact with other systems that also follow REST principles.

**Example of RESTful API Interaction**

Consider a RESTful API for managing a book catalog. A client can use the following requests to interact with the API:

* `GET /books`: Retrieves a list of all books in the catalog.

* `GET /books/1`: Retrieves the details of the book with the ID 1.

* `POST /books`: Creates a new book with the provided title, author, and ISBN.

* `PUT /books/1`: Updates the details of the book with the ID 1.

* `DELETE /books/1`: Removes the book with the ID 1 from the catalog.

**Conclusion**

REST is a powerful and flexible architectural style that is well-suited for developing web APIs. RESTful APIs are simple to understand, easy to implement, and can scale to handle a large number of users. As a result, REST has become the dominant approach for building web-based applications.