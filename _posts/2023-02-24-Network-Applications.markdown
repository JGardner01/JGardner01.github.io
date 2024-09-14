---
title: "Network Tools and Applications"
layout: post
date: 2023-02-24 00:00
tag: 
- python
- networking
- network tools
- sockets
image: null
headerImage: false
projects: true
hidden: false 
description: "This is an overview of the Network Applications Python program implementing ping, traceroute, a web server and proxy server."
category: project
author: James Gardner 
externalLink: false
---
## Overview
This project is a Python program that implements core network functionalities, including Ping, Traceroute, a Web Server and a Proxy Server, all developed using raw Python sockets. It provided insights into real world networking. Each component was developed to explore and demonstrate key networking concepts, allowing me to deepen my understanding of network communication and networking protocols.

### Technologies Used
- **Python:** The language used to develop the networking functionalities.
- **Sockets:** Used for handling network connections.
- **ICMP Protocol:** For implementing the Ping and Traceroute functionalities.
- **TCP/IP Protocols:** For developing the Web Server and Proxy Server.
- **Visual Studio Code:** IDE used for coding and debugging.

## Ping
The ping functionality allows the user to input a web address or an IP address, along with optional parameters such as a timeout duration and number of times to ping the destination (count). The program then sends ICMP Echo requests to the specified target and reports key metrics including packet loss percentage as well as the minimum, maximum and average round trip times (RTTs).

<p align="center">
  <img src="../assets/projectPostContent/networkApplications/pingImage.PNG" alt="ping screenshot" />
  <br/>
  <em>Screenshot of a ping to www.amazon.co.uk</em>
</p>

## Traceroute
The traceroute functionality traces the path packets take to reach a specified host. It sends multiple packets with an increasing Time To Live (TTL) value, allowing each packet to record the routers it passes through until it reaches the destination. At each hop, it attempts to send three packets, recording the Round Trip Times (RTTs) and displaying the route. If a hop is unreachable or a packet is lost, a * is displayed. This feature enables users to visualise the entire path that packets take through the network and can be used to identify where delays or failures occur.

<p align="center">
  <img src="../assets/projectPostContent/networkApplications/tracerouteImage.PNG" alt="traceroute screenshot" />
  <br />
  <em>Screenshot of a traceroute to www.lancaster.ac.uk</em>
</p>

## Web Server
The Web Server functionality is a basic HTTP server that allows users to host and serve local HTML files. Using TCP sockets, the server listens on port 8080 (by default but, can be changed with a command line argument) and serves files requested through a web browser. The server responds with a 200 OK status code if the file exists or a 404 Not Found error if the requested file was not found on the web server.

<p align="center">
  <img src="../assets/projectPostContent/networkApplications/webServerImage.PNG" alt="traceroute screenshot" />
  <br />
  <em>Screenshot of the web server running</em>
</p>

## Proxy Server
The Proxy Server functionality acts as a bridge between the client and a target server, forwarding requests from the client to the intended server and then returning back the server’s responses. Python sockets are used to establish a connection with the target server, retrieve the requested content and send it back to the client. If a request fails, an error message is returned to the client. The proxy server provides an additional layer between the user and the internet and can be configured to listen on a specific port via a command line argument.

<p align="center"> 
  <img src="../assets/projectPostContent/networkApplications/webProxyImage.PNG" alt="web proxy screenshot" width="80%" />
  <br/>
  <em>Screenshot of the proxy server running</em>
</p>

## Conclusion
By developing the Ping, Traceroute, Web Server and Proxy Server functionalities within this project, I gained a deeper understanding of how network communication and protocols operate in real applications as well as knowledge of key network tools. This project also provided insights into client-server communication and network troubleshooting. Overall, this project helped enhance my skills in Python and broadened my understanding of networking tools and protocols.
