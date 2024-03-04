---
layout: default
title: HTTP Status Codes
parent: API Testing
grand_parent: Knowledge
nav_order: 3
---

# HTTP Status Codes

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