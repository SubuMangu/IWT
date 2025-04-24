# Introduction to Web Technologies
- In a network application, two application programmes participate in any communication: one application initiates communication and other accepts it.This is known as **client server interaction**.
- Client requesting serve from server, and the server provides the requested service.

**Features of Client**
- Front end of an application
- Manages user interface portion
- Validates data entered by the user
- Dispatches/sends request to the server programme
- Eg, Web browser are universal client which provide interface to users to request for service,validates data from user,sends request to server and it's a frontend since it is directly displayed in our phone or laptop

**Features of Server**
- Performs back end tasks
- Receives request from clients
- Executes database retrieval and updates
- Manages data integrity
- Dispatches response to clients

**Web Browsers**
- known as universal client since they act as commomn client to acccess all web based applications through www(imp)
- Examples you know

**Server Program\Server:** program that provides service to the client

## Working of Server
In a typical client server interaction, the following thing happens.
1. Client sends a request for a server.
2. Upon receiving the request, the service assigns one thread from the pool to perform the task and wait till further request.
3. The thread executes the requested code.
4. After execution it sends the response back to the client
5. The thread is returned back to the pool

<p align="center"><img src="Images/Screenshot 2025-04-23 211826.png" width="" height=""></p>

## WWW(World Wide Web)
- Information sharing model accessible worldwide.
- It is a collection of electronic documents linked together known as **web pages**
- This architecture depends on three key standards for creating, publishing and finding web documents in the web:
1. **HTML(Hyper Text Markup Language)**
- For creating and editing document 

2. **URL(Uniform Resource Locator)**
- Uniquely identifies each web page or resource in Internet.
- The syntax for URL is:
```
Protocol://ServerDomainName/Path
```
Eg, In the website `http://www.example.com/download`

- `http` is the protocol used
- `example.com` is the ServerDomainName
- `download` is the the relative path

3. **HTTP(Hyper Text Transfer Protocol)**
- It is used for transferring resources between web browsers and web server that are uniquely identified bu URL.
- Used in Application layer of TCP/IP.
- standardises requests send to web server through web browser
- It's a request response protocol(imp)

**HTTP Request-Response**
1. HTTP client initiates a connection to web server through Internet.
2. Once the connexion is established, it sends request message to the server
3. To this request, the server sends a response

<p align="center"><img src="Images/Screenshot 2025-04-24 094236.png" width="" height=""></p>

**HTTP Request**
- HTTP request has three things:
    1. Request Line
    2. Header Lines
    3. Blank Line(to separate header from messange body) 
- The request line in http has three components:
    1. Method to be applied on the resource
    2. Identifier of the resource
    3. Protocol Version in use

- Eg, In a http request line let's say `GET /index.html HTTP/1.1`
    -  `GET` is the method applied
    - `index.html` is the identifier of the resource.
    - `HTTP/1.1` is the protocol name along with it's version
- Three most common methods are used in HTTP request line:
    1. `GET`
    - Used to retrieve data from server
    - Parameters required for this method are send through URLs.
    - Eg, `GET /search?q=books&category=fiction HTTP/1.1` , where  `username=admin` and `password=secret123` are the parameters passed in the body.
    2. `POST`
    - Used to send data to the server, usually to create or update a resource like submitting forms, uploading files, logging in, etc.
    - More secure than GET for sending sensitive information, since data and parameters is sent in the body of the request, not in the URL. 
    - Eg,

```
POST /login HTTP/1.1
Content-Type: application/x-www-form-urlencoded

username=admin&password=secret123
```
- Here, `username=admin` and `password=secret123` are the parameters passed in the body.

    3. `HEAD`
    - Identical to `GET`, but it only retrieves headers — not the body/content.
    - Used to check whether a resource exists, or to fetch metadata (e.g., content length, last modified time) without downloading the actual content.
    Eg, `HEAD /index.html HTTP/1.1`

**HTTP Response**
- The first line of HTTP response is known as **status line**.
- HTTP status line consists of 
    1. Protocol Version
    2. Numeric Status Code
    3. Description of Status code
- Eg, In the given status line `HTTP/1.0 200 OK`
    - `HTTP/1.0` is the protocol along with it's version
    - `200` is the status code
    - `OK` is the decription which means success
- The status code table is given below:

<p align="center"><img src="Images/Screenshot 2025-04-24 102326.png" width="" height=""></p>

- Along with status line, HTTP Response has **HTTP Response Header** describing the following things
    - MIME(Type of data send in response)
    - Date and Time stamp
    - Content size
- **HTTP response message body** contains the required data

## Web Servers
- A Web Server is a server program whose purpose is to serve web pages to other computer when required.
- Most common use of web servers are to host websites.(imp)
- Other uses of Web Server are data storage, running enterprise applications, handling email, ftp and other web uses
- Web servers functions in the the following ways:
1. The website files (HTML, CSS, JavaScript, images, etc.) are stored on the server.
2. When a user enters the website URL in a browser (like www.example.com), a request is sent to the server.
3. The web server processes the request and sends back the appropriate web page or content.
4. The browser displays the website using the content received.
- Web server supports **server side scripting** using Active Server Pages(ASP),PHP or other scripting languages python, java,etc.
- Server side scripting refers to writing the back end of our website.

- Examples of web servers(imp):Apache,Microsoft IIS,

**Apache HTTP Server**
- It played a key role in the early growth of the World Wide Web and was the first web server to serve over 100 million websites.
- Originally developed for Unix-like systems, especially Linux, but now supports many platforms like Windows, macOS, Solaris, FreeBSD, and OS/2.
- It is developed by an open community of developers under the Apache Software Foundation (ASF).
- It supports server-side scripting, dynamic content, and is known for its modular architecture.
- Apache uses **Multi-Processing Modules (MPMs)** to handle multiple requests parallely.

  



