---
layout: default
title: HTTP Methods
parent: API Testing
grand_parent: Knowledge
nav_order: 2
---

# HTTP Methods

HTTP methods are standardized commands or actions that clients (e.g., web browsers, mobile apps) use to communicate with web servers. Each HTTP method defines a specific operation to be performed on a resource identified by a URL (Uniform Resource Locator). HTTP methods are an essential part of the HTTP protocol, which is the foundation of the World Wide Web.

Here are some commonly used HTTP methods:

1. **GET:** The GET method is used to request data from a specified resource. It retrieves data from the server without modifying the resource. GET requests are typically used for retrieving web pages, images, files, and other resources.

2. **POST:** The POST method is used to submit data to be processed to a specified resource. It sends data in the request body, often used for creating new resources, submitting forms, or sending data to a server to be processed.

3. **PUT:** The PUT method is used to update a resource or create a new resource if it does not exist at the specified URL. It replaces the entire resource with the new data provided in the request body.

4. **PATCH:** The PATCH method is similar to PUT but is used to make partial updates to a resource. It updates only the fields specified in the request body, leaving other fields unchanged.

5. **DELETE:** The DELETE method is used to request the removal of a resource from the server. It deletes the resource at the specified URL.

6. **HEAD:** The HEAD method is similar to GET but retrieves only the headers of the response, not the actual data content. It is often used to check the status and metadata of a resource without downloading the entire resource.

7. **OPTIONS:** The OPTIONS method is used to retrieve information about the communication options available for the target resource. It can provide details about supported HTTP methods, headers, and other communication parameters.