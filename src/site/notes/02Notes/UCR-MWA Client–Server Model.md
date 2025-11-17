---
{"dg-publish":true,"permalink":"/02-notes/ucr-mwa-client-server-model/","tags":["#notes/atomic"]}
---

**Link to Course**: [[02Notes/Curriculum Building a Modern Web App UCR Starter Project\|Curriculum Building a Modern Web App UCR Starter Project]]  - [[02Notes/Part 1 Web Foundations & Building the First Full-Stack App\|Part 1 Web Foundations & Building the First Full-Stack App]] 

---
## Overview of Client Server Architecture

A client server model (also called  client-server architecture) is a way of structuring your system such that 

- **Clients/Frontend**: Devices or software that request services or resources. This is **how a user will interact with our application** (example browser, mobile app )

- **Servers**: Machines or software that provide those services or resource. (example web server, database server). Defines **what our application does once** it receives a request from a user, it can be something such as transforming, retrieving or creating some information.

- **[[02Notes/Databases\|Databases]]**: Where we store and retrieve data from. 
- **[[Communication Protocols\|Communication]]**: In this model communication between the client and server is done over a [[02Notes/Networking\|network]] using defined protocols(example [[02Notes/HTTP Streaming\|HTTP]],  [[02Notes/TCP & IP Model\|TCP/IP]])

---

# Client Server Architecture Is Everywhere

We interact with client server application all the time.  For instance when we access You tube we want to access some video. On the client side we simply click on the video we want. On the backend the server will look for the video and return it to us.  Finally the client will render the video 


## Examples In Real Life 

- **[[Web Applications\|Web Applications]]**: Browser (client) → Web server → Database
- **Mobile apps**: App (client) makes API calls to backend servers
- **Email**: Mail client (Outlook, Gmail app) requests SMTP/IMAP/POP services

# High Level Overview

1. Client initiates a request (ex `YouTube.com`)
2. The request travels over a network (possibly via [[DNS\|DNS]])
3. Server receives the request
4. Server process the request (example querying a database and looking for the video you looked up)
5. The server creates a response (example HTML, JSON , video)
6. The server sends back the response over network
7. Client receives the response and renders / uses it

---
# Variants and Layers: Single, Two, Three and N tier

Client-server systems often are designed with multiple layers (tiers) to separate concerns and improve maintainability:

![Pasted image 20251116151705.png|center](/img/user/Attachments/Pasted%20image%2020251116151705.png)

1. **One Tier Architecture**. All components are grouped together 
2. **Two Tier Architecture**: Two components are grouped together (can be any way you want). 
 3. **Three Tier Architecture**: Each component is separated
4. **N Tier Architecture**: You can have as many tiers as you want

This layering helps in modularizing, securing, scaling, and maintaining complex applications


----
# Resources

- [Client Server Architecture System Design Basics](https://www.youtube.com/watch?v=yioOQ4ItYuo): A short 5 minute view covering the basics of [[02Notes/Client-Server Architecture\|Client-Server Architecture]]
-  [Everything You NEED to Know About WEB APP Architecture (youtube.com)](https://www.youtube.com/watch?v=sDlCSIDwpDs): A deeper dive really good video showcases actual examples for better understanding.
