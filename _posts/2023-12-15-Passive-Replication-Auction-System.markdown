---
title: "Passive Replication Auction System"
layout: post
date: 2023-12-15 00:00
tag:
- university year 3
- java
- RMI
- distributed systems
- passive replication
image: null
headerImage: false
projects: true
hidden: false 
description: "This is an overview of the Passive Replication Secure Auction System Java program."
category: project
author: James Gardner 
externalLink: false
---
## Overview
The Passive Replication Auction System project is a distributed system created using Java and Remove Method Invocation (RMI) registry, developed during my third year at Lancaster University. It is designed to provide a reliable and fault tolerant auction system platform where multiple clients can seamlessly interact with the auction system, even if server failures occur. This system consists of a stateless front end, passive replication with multiple auction server replicas and clients that interact with the front end.

## System Architecture
The Passive Replication Auction System is a distributed system consisting of the following key components:

#### Stateless Front End
The stateless front end is responsible for communicating with the clients. It forwards all client requests to and from the designated primary replica without storing any auction data itself. The design ensures that the system remains simple for all clients, allowing  them to interact with the auction platform without needing to be aware of the underlying replica management or which server is currently acting as the primary replica. Keeping the front end stateless ensures that it is lightweight and removes risks of data loss from failures at this layer.

Key functions of the front end are:
- **Primary Replica Selection:** The front end checks the RMI Registry to locate and identify the primary replica, forwarding client requests to it. If the primary fails, the front end selects and promotes another replica to primary.
- **Fault-Tolerant Request Handling:** The front end checks for replica failures before forwarding requests, ensuring the system continues to operate by selecting a new primary when needed.

#### Replica Management and Passive Replication
The auction system uses multiple replica servers to maintain consistent auction state data. All replicas are synchronised with the primary replica, ensuring that they all hold the exact same auction data at all times. Each replica is updated with its count number of processed requests to easily ensure that all replicas are up to date. This synchronisation ensures that even if the primary replica fails, another replica can be promoted to primary replica without any loss of auction data. The use of passive replication helps the system recover from faults and provides a high availability to users.
- **Primary Replica:** Only the primary replica processes client requests. The primary replica is responsible for updating other replicas to keep the system consistent.
- **Fault Recovery Process:** In case the primary replica fails, a new replica is promoted to primary by the front-end. Each replica maintains an identical state to ensure smooth failover. Replicas that experience failures can rejoin the system once they recover. When a replica starts, it fetches the most recent state from the primary replica to ensure it has up-to-date auction data.
- **State Synchronization:** Every replica is updated with the auction data after each request is processed by the primary replica, ensuring no data inconsistency across replicas.
- **Complete Turnover:** The system remains fully operational even if all initial replicas fail and are replaced by new ones.

The system includes a bash file that automates the setup of the auction system, by starting the RMI registry, front end and the replica servers. The script allows users to easily add new replicas, each in a separate process.

<p align="center">
  <img src="../assets/projectPostContent/passiveReplicationAuctionSystem/SystemDesign.png" alt="system architecture diagram" width="50%"/>
  <br/>
  <em>Diagram of the system architecture</em>
</p>

## Client Program Functionality
1. **User Registration:** Clients can register with their email to get a unique user ID. This user ID is necessary for participating in auctions.
2. **Auction Creation:** Registered users can create new auctions by specifying details such as the item name, description and reserve price.
3. **Bidding:** Registered clients can place bids on active auctions. Bids are only accepted if they are higher than the current highest bid and meet the reserve price.
4. **Auction Listing:** Clients can view all active auctions, including information such as the item ID, description and highest bid.
5. **Auction Closure:** Only the auction creator can close the auction. If the reserve price is met, the item is sold to the highest bidder. The winning bidder's information is stored and displayed upon closure.

## Demo

## Conclusion
Developing this Passive Replication Auction System project significantly deepened my understanding of distributed systems, particularly in the areas of fault tolerance and replication. Implementing passive replication in this project highlighted the importance of maintaining system state consistency and ensuring a seamless failover process in the event of server failures. This project also provided practical experience with Java RMI, allowing me to explore remote method invocations and the complexities of managing communication within a distributed system. Overall, this project provided a valuable opportunity to explore the intricacies of designing a reliable, scalable system and reinforced key concepts such as redundancy and fault recovery, which are essential for building real-world distributed applications.
