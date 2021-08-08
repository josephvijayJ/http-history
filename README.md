# http-history

# Evolution of Http

HTTP (HyperText Transfer Protocol) is the underlying protocol of the World Wide Web. Developed by Tim Berners-Lee and his team between 1989-1991, HTTP has seen many changes, keeping most of the simplicity and further shaping its flexibility. HTTP has evolved from an early protocol to exchange files in a semi-trusted laboratory environment, to the modern maze of the Internet, now carrying images, videos in high resolution and 3D.

# Invention of the World Wide Web
In 1989, while he was working at CERN, Tim Berners-Lee wrote a proposal to build a hypertext system over the Internet. Initially calling it the Mesh, it was later renamed to World Wide Web during its implementation in 1990. Built over the existing TCP and IP protocols, it consisted of 4 building blocks:

A textual format to represent hypertext documents, the HyperText Markup Language (HTML).
A simple protocol to exchange these documents, the HypertText Transfer Protocol (HTTP).
A client to display (and accidentally edit) these documents, the first Web browser called WorldWideWeb.
A server to give access to the document, an early version of httpd.
These four building blocks were completed by the end of 1990, and the first servers were already running outside of CERN by early 1991. On August 6th 1991, Tim Berners-Lee's post on the public alt.hypertext newsgroup is now considered as the official start of the World Wide Web as a public project.

The HTTP protocol used in those early phases was very simple, later dubbed HTTP/0.9, and sometimes as the one-line protocol.

# HTTP/0.9 – The one-line protocol
The initial version of HTTP had no version number; it has been later called 0.9 to differentiate it from the later versions. HTTP/0.9 is extremely simple: requests consist of a single line and start with the only possible method GET followed by the path to the resource (not the URL as both the protocol, server, and port are unnecessary once connected to the server).

**HTTP/1.0 – Building extensibility**
**HTTP/0.9** was very limited and both browsers and servers quickly extended it to be more versatile:

Versioning information is now sent within each request (HTTP/1.0 is appended to the GET line)
A status code line is also sent at the beginning of the response, allowing the browser itself to understand the success or failure of the request and to adapt its behavior in consequence (like in updating or using its local cache in a specific way)
The notion of HTTP headers has been introduced, both for the requests and the responses, allowing metadata to be transmitted and making the protocol extremely flexible and extensible.

With the help of the new HTTP headers, the ability to transmit other documents than plain HTML files has been added (thanks to the Content-Type header).
At this point, a typical request and response looked like this:


These novelties have not been introduced as concerted effort, but as a try-and-see approach over the 1991-1995 period: a server and a browser added one feature and it saw if it got traction. A lot of interoperability problems were common. In November 1996, in order to solve these annoyances, an informational document describing the common practices has been published, RFC 1945. This is the definition of HTTP/1.0 and it is notable that, in the narrow sense of the term, it isn't an official standard.

# HTTP/1.1 – The standardized protocol
In parallel to the somewhat chaotic use of the diverse implementations of HTTP/1.0, and since 1995, well before the publication of HTTP/1.0 document the next year, proper standardization was in progress. The first standardized version of HTTP, HTTP/1.1 was published in early 1997, only a few months after HTTP/1.0.

# HTTP/1.1 clarified ambiguities and introduced numerous improvements:

A connection can be reused, saving the time to reopen it numerous times to display the resources embedded into the single original document retrieved.
Pipelining has been added, allowing to send a second request before the answer for the first one is fully transmitted, lowering the latency of the communication.
Chunked responses are now also supported.
Additional cache control mechanisms have been introduced.
Content negotiation, including language, encoding, or type, has been introduced, and allows a client and a server to agree on the most adequate content to exchange.
Thanks to the Host header, the ability to host different domains at the same IP address now allows server colocation.

## versions and Features

The Hypertext Transfer Protocol (HTTP) is an application layer protocol in the Internet protocol suite model for distributed, collaborative, hypermedia information systems. HTTP is the foundation of data communication for the World Wide Web, where hypertext documents include hyperlinks to other resources that the user can easily access, for example by a mouse click or by tapping the screen in a web browser.

Development of HTTP was initiated by Tim Berners-Lee at CERN in 1989. Development of early HTTP Requests for Comments (RFCs) was a coordinated effort by the Internet Engineering Task Force (IETF) and the World Wide Web Consortium (W3C), with work later moving to the IETF.

HTTP/1 was first documented (as version 1.1) in 1997.

HTTP/2 is a more efficient expression of HTTP's semantics "on the wire", and was published in 2015, and is used by 45% of websites; it is now supported by virtually all web browsers and major web servers over Transport Layer Security (TLS) using an Application-Layer Protocol Negotiation (ALPN) extension where TLS 1.2 or newer is required.

HTTP/3 is the proposed successor to HTTP/2, and two-thirds of web browser users (both on desktop and mobile) can already use HTTP/3, on the 20% of websites that already support it; it uses QUIC instead of TCP for the underlying transport protocol. Like HTTP/2, it does not obsolete previous major versions of the protocol. Support for HTTP/3 was added to Cloudflare and Google Chrome first, and is also enabled in Firefox.
