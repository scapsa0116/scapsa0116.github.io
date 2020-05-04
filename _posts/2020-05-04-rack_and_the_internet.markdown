---
layout: post
title:      "Rack and the Internet"
date:       2020-05-04 19:01:32 +0000
permalink:  rack_and_the_internet
---


### The internet operates based on conversations between the client  and the server. By typing in that URL into the browser, you are requesting a web page. The browsers and servers talk is controlled by a contract or protocol.Specifically it is a protocol created by Tim Berners-Lee called the Hyper Text Transfer Protocol or HTTP.  Lets brake down an HTTP

#### EX. 

#### https://github.com/new 
#### https:// - the protocol
#### github.com - the domain
#### /new - the resource


### The *protocol* is the way we're sending our request, the *domain* name is a string of characters that identifies the unique location of the web and the *resource* is the particular part of the website we want to load.

### A request to HTTP is an action that we would like the server to do. We do this with HTTP Verbs.
## VERB	Description
#### HEAD	Asks for a response like a GET but without the body
#### GET	Retrieves a representation of a resource
#### POST	Submits data to be processed in the body of the request
#### PUT	Uploads a representation of a resource in the body of the request
#### DELETE	Deletes a specific resource
#### TRACE	Echoes back the received request
#### OPTIONS	Returns the HTTP methods the server supports
#### CONNECT	Converts the request to a TCP/IP tunnel (generally for SSL)
#### PATCH	Apply a partial modification of a resource

#### GET is an request of "hey server, please GET me this resource"
#### POST is a request of sending data from user to the server.
#### Once the server receives the request, it will do some processing and then send a response back. A good framework to build applications is gemCorneal, VERB are placed in the controllers, and usualy is the path of how the code is running. 

### Status Code
#### Statuse code is a response, usualy presented as an number. The numbers are separated into categories based on their first digit

#### 100's - informational
#### 200's - success
#### 300's - redirect
#### 400's - error
#### 500's - server error

## Rack is a gem, a common foundation for all web-servers. 
#### To work with Rack, we need to create a thing that responds to a single method: #call.
 #### Files that are used by Rack end with .ru instead of .rb because they're normally loaded with a command called rackup.  This is an example of Rack server: 
 
 ### require 'rack'
 
##### Instances of Proc automatically have a call method that runs the block that
##### they're initialized with.
### my_server = Proc.new do
### [200, { 'Content-Type' => 'text/html' }, ['<em>Hello</em>']]
### end
 
### run my_server

#### Rails, Sinatra, any web programming framework is a way to organize the code that fills out that third Array element in the Rack responses. The server setup code lives in the rackup file and our application logic lives in a class that's referenced by the run command in the rackup file.
