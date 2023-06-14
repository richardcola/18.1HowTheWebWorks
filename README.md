# 18.1HowTheWebWorks

What is HTTP?
Hypertext Transfer Protocol

What is a URL?
uniform resource locator

What is DNS?
domain name system

What is a query string?
the part of a URL that follows the symbol, ?, and it contains parameters for a web request

What are two HTTP verbs and how are they different?
POST and GET.  POST submits data to a server to create a new resource while GET retreives data from the server.

What is an HTTP request?
message snet by a client to a server to initiate a specific action or get a resource

What is an HTTP response?
a message sent by a server

What is an HTTP header? Give a couple examples of request and response headers you have seen.
It is part of both the request and response messages consisting of a field name, a corresponding value and a colon used to separate the two.
User-Agent (Request Header):

An example value found in a HTTP header is as follows: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/80.0.3987.163 Safari/537.36 The User-Agent header is commonly found in HTTP requests. It provides information about the client application or web browser making the request. Developers can use this header to determine the type of client and its capabilities. It helps in tailoring the response to suit the client's requirements.
Content-Type (Request and Response Header):

Example Value (Request): Content-Type: application/json
Example Value (Response): Content-Type: text/html; charset=utf-8
Description: The Content-Type header indicates the media type or format of the data being sent or received. In request headers, developers can specify the format of the data they are sending to the server. In response headers, it informs the client about the format of the data in the response body. Common values include "application/json" for JSON data, "text/html" for HTML content, "image/png" for PNG images, and so on.
Accept (Request Header):

Example Value: Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,/;q=0.8
Description: The Accept header is used by the client to specify the media types it can handle in the response. It informs the server about the preferred content types. The value may include multiple types with associated quality factors (q-values) to indicate their relative preference.
Cache-Control (Response Header):

Example Value: Cache-Control: max-age=3600
Description: The Cache-Control header defines caching directives for both the client and intermediate caching proxies. It specifies how the response should be cached and for how long. Developers can set directives like "max-age" to indicate the maximum time the response should be considered fresh, "no-cache" to always validate the response with the server, or "private" to specify that the response is specific to the user and should not be cached publicly.

What are the processes that happen when you type “http://somesite.com/some/page.html” into a browser?
URL parsing, DNS resolution, TCP connection establishment, HTTP request, server processing, HTTP response and rendering

Part Two: Practice Tools
Using curl, make a GET request to the icanhazdadjoke.com API to find all jokes involving the word “pirate”
curl -H "Accept: application/json" "https://icanhazdadjoke.com/search?term=pirate"


Use dig to find what the IP address is for icanhazdadjoke.com
172.67.198.173 or 104.21.66.15

Make a simple web page and serve it using python3 -m http.server. Visit the page in a browser.
<!DOCTYPE html>
<html>
<head>
  <title>My Simple Web Page</title>
</head>
<body>
  <h1>Welcome to My Simple Web Page!</h1>
  <p>This is a basic web page served using Python's built-in HTTP server.</p>
</body>
</html>

Saved the above html in a file named, index-mPytonServer.html, in the following diretory, c:\Users\richa\Downloads\USFCertificate.


Part Three: Explore Dev Tools
Build a very simple HTML form that uses the GET method (it can use the same page URL for the action) when the form is submitted.

Add a field or two to the form and, after submitting it, explore in Chrome Developer tools how you can view the request and response headers.

Edit the page to change the form type to POST, refresh in the browser and re-submit. Do you still see the field in the query string? Explore in Chrome how you can view the request and response headers, as well as the form data.

Part Four: Explore the URL API
At times, it’s useful for your JavaScript to look at the URL of the browser window and change how the script works depending on parts of that (particularly the query string).

Read about the URL API

Try some of the code examples in the Chrome Console so that you can get comfortable with the basic methods and properties for instances of the URL class.
