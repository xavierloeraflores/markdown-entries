---
title: "Request Response Communication Pattern"
date: 2024-07-03T03:15:50-08:00
draft: false
tags:
    [
        "Software Engineering",
        "Computer Science",
        "Backend",
        "Fullstack Development",
        "Request",
        "Response",
        "REST",
        "SOAP",
        "TCP",
        "GraphQL",
        "HTTP",
        "DNS",
        "SSH",
        "RPC",
        "Server",
        "API",
        "Communication Protocol",
        "SQL",
        "Database Protocols",
    ]
---

The request-response model is a communication pattern used in computing where a client sends a request to a server, and the server responds to the request. This model is used in various communication protocols and APIs to exchange data between clients and servers widely used in web development, networking, and distributed systems.

Examples of this request response pattern can be seen in following use cases:

- Protocols
    - HTTP
    - DNS
    - SSH
    - RPC
    - TCP

- APIS
    - REST
    - SOAP
    - GraphQL

## Request Response Model
The following steps are involved in the request-response model pattern:

- Client sends a request to the server
- Server parses the request
- Server processes the request
- Server sends a response to the client
- Client parses the response
- Client processes the response

![Request Response Model](/notes/attachments/images/request-response.png)

The diagram above shows the request-response model where the client sends a request to the server, and the server responds to the request. The client and server communicate over a network using a communication protocol such as HTTP, TCP, or RPC. 

> 🗒️ **Note:** Parsing messages takes time on both the client and server and should seen as its own step prior to any processing done with the content of the messages. 


## Anatomy of a HTTP Request/Response
```
START LINE (REQUEST LINE OR STATUS LINE)
<CRLF>
HEADERS
<CRLF>
BODY
```
The start line of the request or response message is called the request/status line. If the message is a request, it contains a Request line which includes the HTTP method, request target, and HTTP version. If the message is a response, it contains a Status line which includes the HTTP version, status code, and reason phrase. The request/status line is followed by a sequence of headers, each on a new line. The message body is used to send data from the client to the server in a request or from the server to the client in a response. All parts of the message are separated by a carriage return line feed (CRLF) sequence.

## \<CRLF\>
CRLF also known as Carriage Return Line Feed is a sequence of two characters that is used to specify a new line in a text file. It is used to indicate the end of a line of text and the start of a new one. 

The two characters are:
- Carriage Return (CR) - `\r`
- Line Feed (LF) - `\n`
- Together (CRLF) `\r\n`

## HTTP Version

The HTTP version defines the structure of the request message and acts as an indicator for the expected behavior & http version from the server. It is included on both the request's request line and the response's status line.

The following are some of the HTTP versions:

- HTTP/0.9
- HTTP/1.0
- HTTP/1.1
- HTTP/2.0
- HTTP/3.0

## Request Line

```http
GET / HTTP/1.0
```

The Request Line is the first line of the request message. It contains the following parts:

- HTTP Method
- Request Target
- HTTP Version

These parts map to the following components from our sample request:

- HTTP Method: `GET`
- Request Target: `/`
- HTTP Version: `HTTP/1.0`

Another Example Request Line:

```http
POST /pictures HTTP/1.1
```
- HTTP Method: `POST`
- Request Target: `/pictures`
- HTTP Version: `HTTP/1.1`

### HTTP Methods
HTTP methods are used to indicate the desired action taken on the resource identified by the request target. Some servers may not support all methods and may return an error if an unsupported method is used. Specifying the correct method is important since some servers may have different behavior for different methods bound to the same request target.

The following are HTTP methods:

- CONNECT
- DELETE
- GET
- HEAD
- OPTIONS
- PATCH
- POST
- PUT
- TRACE

### Request Target
The request target is the resource that the client is requesting from the server. It can be represented in four different forms:


#### Origin Form
Origin form is the most common form as it features a absolute path to the resource and is typically used with the following methods: GET, POST, PUT, DELETE, PATCH, HEAD, and TRACE.
```
/
/resource
/resource/file.txt
/resource/file.txt?param1=value1
/resource/file.txt?param1=value1&param2=value2
```

#### Absolute Form
Absolute form is used commonly when connecting to an external proxy server. It features the full URL of the resource. It is used with the following methods: GET, POST, PUT, DELETE, PATCH, HEAD, and TRACE.
```
https://website.com/
https://website.com/resource
https://website.com/resource/file.txt
https://website.com/resource/file.txt?param1=value1
https://website.com/resource/file.txt?param1=value1&param2=value2
```

#### Authority Form
Authority form is used when connecting to a proxy server and features the hostname and port number of the resource prefixed by a colon `:`. It is only used with the CONNECT method when setting up an HTTP tunnel.

```
https://website.com:80/
https://website.com:80/resource
```

#### Asterisk Form
Asterisk form represented by an asterisk to represent the server and is used with the OPTIONS method to request information about the server's capabilities.

```
*
```

Example Asterisk Form Request Line
```http
OPTIONS * HTTP/1.1
```




## Status Line

```http
HTTP/1.1 200 OK
```

The Status Line is the first line of the response message. It contains the following parts:

- HTTP Version
- Status Code
- Reason Phrase

These parts map to the following components from our sample request:

- HTTP Version: `HTTP/1.1`
- Status Code: `200`
- Reason Phrase: `OK`

Another Example Response Status Line:

```http
HTTP/1.1 404 Not Found
```
- HTTP Version: `HTTP/1.1`
- Status Code: `404`
- Reason Phrase: `Not Found`

### Status Codes & Reason Phrases
Status codes are used to indicate the result of the request. They are three-digit numbers that are grouped into five classes:

- 1xx: Informational
- 2xx: Success
- 3xx: Redirection
- 4xx: Client Error
- 5xx: Server Error


Reason phrases are used to provide a human-readable explanation of the status code. They are not required to be accurate and are often used for debugging purposes by humans. 

Some common status codes and reason phrases include:

- 200 OK
- 201 Created
- 202 Accepted
- 301 Moved Permanently
- 302 Found
- 400 Bad Request
- 401 Unauthorized
- 403 Forbidden
- 404 Not Found
- 500 Internal Server Error
- 501 Not Implemented
- 503 Service Unavailable


## Headers
```http
Content-Type: application/json
```

Headers are key-value pairs that provide additional information about the request or response. They are used to pass information such as the content type, content length, cookies, and more. They are structured as case-insensitive strings each paired with a value of a structure determined by the key string following a colon `:` to separate the pair.  Headers are separated by a carriage return line feed (CRLF) sequence and are terminated by an empty line. 

Headers can be classified into the following categories:

- General Headers
- Request/Response Headers
- Representation Headers (_AKA Entity Headers in older versions of HTTP_)

#### General Headers
General headers are used in both requests and responses and provide information about the message itself. They include headers such as `Cache-Control`, `Connection`, `Upgrade`, and `Via`.

#### Request Headers
Request headers are used in requests to provide additional information about the client or the resource being requested. They include headers such as `Host`, `User-Agent`, `Accept`, and `Authorization`.

#### Response Headers
Response headers are used in responses to provide additional information about the server or the resource being returned. They include headers such as `Vary`, `Accept-Ranges`, `Server`, and `Content-Encoding`.

#### Representation Headers
Representation headers are used in both requests and responses and are used to provide information about the representation of the resource being requested or returned. They include headers such as `Content-Type`, `Content-Range`, `Content-Encoding`, and `Content-Language`.

## Body
```http
{
    "param1": "value1",
    "param2": "value2"
}
```

The body of the message is optionally used to send different types of data such as text, images, videos, or binary data. The body is separated from the headers that define its structure by an empty line and is terminated by the end of the message. The body is used to send data on PUT, POST, and PATCH requests and on responses that return data to the requesting client.

Bodies can be classified into the following categories:
- **Single Resource Bodies**: Consists of a single resource such as a JSON object, XML document, or plain text defined by the `Content-Type` & `Content-Length` headers.
- **(Chunked)Single Resource Body**: Consists of a single resource of a potentially unknown length encoded in chunks with the `Transfer-Encoding: chunked` header.
- **Multiple Resource Bodies**: Consists of multipart body parts containing different resources usually defined by the `Content-Type: multipart/form-data` header.


## More Examples

Anatomy
```
START LINE (REQUEST LINE OR STATUS LINE)
<CRLF>
HEADERS
<CRLF>
BODY
```

Human Readable Sample Request
```http
POST /upload HTTP/1.1
Host: localhost:4221
User-Agent: foobar/1.2.3
Content-Type: application/json
{
    "param1": "value1",
    "param2": "value2"
}

```

Raw Sample Request
```http
POST /upload HTTP/1.1
\r\n
Host: localhost:4221\r\n
User-Agent: foobar/1.2.3\r\n
Content-Type: application/json\r\n
\r\n
{
    "param1": "value1",
    "param2": "value2"
}
```

Human Readable Sample Response
```http
HTTP/1.1 200 OK
Content-Type: application/json
{
    "status": "success",
    "message": "File uploaded successfully"
}
```

Raw Sample Response
```http
HTTP/1.1 200 OK
Content-Type: application/json\r\n
\r\n
{
    "status": "success",
    "message": "File uploaded successfully"
}
```


## Resources

- [MDN Web Docs - HTTP Messages](https://developer.mozilla.org/en-US/docs/Web/HTTP/Messages)
- [MDN Web Docs - HTTP Headers](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers)
- [MDN Web Docs - Response Header](https://developer.mozilla.org/en-US/docs/Glossary/Response_header)
- [MDN Web Docs - Request Header](https://developer.mozilla.org/en-US/docs/Glossary/Request_header)
- [MDN Web Docs - Representation Header](https://developer.mozilla.org/en-US/docs/Glossary/Representation_header)
