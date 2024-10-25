# HTTP response status codes
-HTTP response status codes indicate whether a specific HTTP request has been successfully completed.

Responses are grouped classes, the five classes are summarized bellow:

# 1. Informational responses

### <ins>Types of informational responses</ins>

<h3 style ="color:green">100 Continue</h3>
This interim response indicates that the client should continue the request or ignore the response if the request is already finished.

<h3 style ="color:green">101 Switching Protocols</h3>
This code is sent in response to an Upgrade request header from the client and indicates the protocol the server is switching to.

<h3 style ="color:green">102 Processing Deprecated</h3>
This code was used in WebDAV contexts to indicate that a request has been received by the server, but no status was available at the time of the response.

<h3 style ="color:green">103 Early Hints</h3>
This status code is primarily intended to be used with the Link header, letting the user agent start preloading resources while the server prepares a response or preconnect to an origin from which the page will need resources.

# 2. Successful responses

 <ins>Types of Successful responses</ins>


<h3 style ="color:green">200 OK</h3>

 - The request succeeded. The result and meaning of "success" depends on the HTTP method

    - GET: The resource has been fetched and transmitted in the message body.
    - HEAD: The headers are included without any message body.
    - PUT or POST: The resource describing the result of the action is transmitted in the message body.
    - TRACE: The message body contains the request as received by the server.

<h3 style ="color:green">201 Created</h3>
The request succeeded, and a new resource was created as a result. This is typically the response sent after POST requests, or some PUT requests.

<h3 style ="color:green">202 Accepted</h3>
The request has been received but not yet acted upon. This status is useful in scenarios like batch processing. 

<h3 style ="color:green">203 Non-Authoritative Information</h3>
 The returned metadata is collected from a third-party copy, not exactly the same as from the origin server. 

<h3 style ="color:green">204 No Content</h3>
 The returned metadata is collected from a third-party copy, not exactly the same as from the origin server. 

<h3 style ="color:green">205 Reset Content</h3>
Tells the user agent to reset the document which sent this request.

<h3 style ="color:green">206 Partial Content</h3>
Tells the user agent to reset the document which sent this request.

<h3 style ="color:green">207 Multi-Status (WebDAV)</h3>
Conveys information about multiple resources, for situations where multiple status codes might be appropriate.

<h3 style ="color:green">208 Already Reported (WebDAV)</h3>

Used to avoid enumerating internal members of a collection more than once.

<h3 style ="color:green">226 IM Used (HTTP Delta encoding)</h3>

 The server fulfilled a GET request and applied a delta encoding instance-manipulation to the response.

# 3. Redirection messages

<ins>Types of Redirection Messages</ins>

<h3 style ="color:green">300 Multiple Choices</h3>
 There are multiple options for the resource requested, and the user should choose one.

<h3 style ="color:green">301 Moved Permanently</h3>
The URL of the requested resource has been moved permanently. The new URL is given in the response.

<h3 style ="color:green">302 Found</h3>
This response code means that the URI of requested resource has been changed temporarily. Further changes in the URI might be made in the future, so the same URI should be used by the client in future requests. 

<h3 style ="color:green">303 See Other</h3>
Directs the client to retrieve the resource at another URI using a GET request.

<h3 style ="color:green">304 Not Modified</h3>

This is used for caching purposes. It tells the client that the response has not been modified, so the client can continue to use the same cached version of the response.

<h3 style ="color:green">305 Use Proxy </h3>
Defined in a previous version of the HTTP specification to indicate that a requested response must be accessed by a proxy. It has been deprecated due to security concerns regarding in-band configuration of a proxy.

<h3 style ="color:green">306 unused</h3>
This response code is no longer used; but is reserved. It was used in a previous version of the HTTP/1.1 specification.


<h3 style ="color:green">307 Temporary Redirect</h3>
The server sends this response to direct the client to get the requested resource at another URI with the same method that was used in the prior request. This has the same semantics as the 302 Found response code, with the exception that the user agent must not change the HTTP method used: if a POST was used in the first request, a POST must be used in the redirected request.

<h3 style ="color:green">308 Permanent Redirect</h3>
This means that the resource is now permanently located at another URI, specified by the Location response header. This has the same semantics as the 301 Moved Permanently HTTP response code, with the exception that the user agent must not change the HTTP method used: if a POST was used in the first request, a POST must be used in the second request.


# 4. Client Error Responses
<ins>Types of Client Error Responses</ins>

<h3 style="color:green">400 Bad Request</h3>
 The server cannot process the request due to a client error (e.g., malformed syntax).

<h3 style="color:green">401 Unauthorized</h3> 
The client must authenticate to receive the requested response.

<h3 style="color:green">402 Payment Required</h3> 
This code is reserved for future use, related to payment systems. 

<h3 style="color:green">403 Forbidden</h3> 
The client does not have the rights to access the content.

<h3 style="color:green">404 Not Found</h3> 
The server cannot find the requested resource.

<h3 style="color:green">405 Method Not Allowed</h3>
The HTTP method is not allowed for the requested resource. 

<h3 style="color:green">406 Not Acceptable</h3> 
The server cannot provide a response that matches the client's content negotiation. 

<h3 style="color:green">407 Proxy Authentication Required</h3> The client must authenticate with a proxy. 

<h3 style="color:green">408 Request Timeout</h3>
The server timed out waiting for the request.

<h3 style="color:green">409 Conflict</h3> 
The request conflicts with the current state of the server. 

<h3 style="color:green">410 Gone</h3> 
The requested content has been permanently deleted. 

<h3 style="color:green">411 Length Required</h3> 
The request did not specify the length of its content, which is required by the server. 

<h3 style="color:green">412 Precondition Failed</h3> 
One or more conditions in the request headers are false. 

<h3 style="color:green">413 Content Too Large</h3> 
The request body is too large for the server to process.

<h3 style="color:green">414 URI Too Long</h3> 
The URI requested is longer than the server can process.

<h3 style="color:green">415 Unsupported Media Type</h3>
 The request entity's media format is unsupported. 
 
 <h3 style="color:green">416 Range Not Satisfiable</h3> 
 The requested range cannot be fulfilled.
 
<h3 style="color:green">417 Expectation Failed</h3> 
The server cannot meet the expectations indicated in the request's Expect header. 

<h3 style="color:green">418 I'm a Teapot</h3>
This is an Easter egg status code indicating the server is a teapot (RFC 2324). 

<h3 style="color:green">421 Misdirected Request</h3> 
The request was directed at a server that is not able to produce a response.

 <h3 style="color:green">422 Unprocessable Content (WebDAV)</h3> 
 The request is well-formed but could not be processed. 
 
 <h3 style="color:green">423 Locked (WebDAV)</h3> 
 The resource is currently locked. 
 
 <h3 style="color:green">424 Failed Dependency (WebDAV)</h3> 
 The request failed because it depended on another request. 
 
 <h3 style="color:green">425 Too Early Experimental</h3> 
 The server is unwilling to process the request due to the risk of replay attacks. 
 
 <h3 style="color:green">426 Upgrade Required</h3> 
 The server refuses to process the request unless the client upgrades to a different protocol.

<h3 style="color:green">428 Precondition Required</h3> 
The server requires that the request be conditional to avoid the 'lost update' problem. 

<h3 style="color:green">429 Too Many Requests</h3> 
The user has sent too many requests in a given time frame (rate limiting). 

<h3 style="color:green">431 Request Header Fields Too Large</h3> The request's header fields are too large for the server to process. 

<h3 style="color:green">451 Unavailable for Legal Reasons</h3> The resource is unavailable due to legal reasons.


# 5. Server Error Responses

<ins>Types of Server Error Responses</ins>

<h3 style="color:green">500 Internal Server Error</h3> 
The server encountered a situation it doesn't know how to handle. 

<h3 style="color:green">501 Not Implemented</h3> 
The server does not support the functionality required to fulfill the request. 

<h3 style="color:green">502 Bad Gateway</h3> 
The server, acting as a gateway, received an invalid response from an upstream server.

 <h3 style="color:green">503 Service Unavailable</h3> 
 The server is not ready to handle the request, typically due to maintenance or overload. 
 
 <h3 style="color:green">504 Gateway Timeout</h3> 
 The server acting as a gateway did not receive a timely response. 
 
 <h3 style="color:green">505 HTTP Version Not Supported</h3>
  The server does not support the HTTP version used in the request





