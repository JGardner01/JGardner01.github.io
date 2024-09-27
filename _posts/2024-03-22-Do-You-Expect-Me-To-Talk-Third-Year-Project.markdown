---
title: "Do You Expect Me To Talk? (Third Year Project)"
layout: post
date: 2024-03-22 00:00
tag: 
- university year 3
- javascript
- node.js
- html
- css
- webrtc
image: null
headerImage: false
projects: true
hidden: false 
description: "This is an overview of my third year project."
category: project
author: James Gardner 
externalLink: false
---
## Overview
The Do You Expect Me To Talk? project is my third year project that I developed at Lancaster University. This project addresses key challenges in modern digital communication by creating an intuitive, no app based system that prioritises privacy, ensures universal accessibility, and provides a user friendly experience. The project provides users with a platform to engage in voice, video and text based communication as well as the ability to share files over a local network, all without requiring personal information or relying on centralised servers.

Created using HTML, CSS, JavaScript, Node.js and WebRTC, and then deployed on Heroku, the application enables multiple devices to form a Personal Area Network (PAN), allowing seamless peer to peer communication. This includes the exchange of messages, media files and real time video and voice streams. By using WebRTC to facilitate the media streams and data transfer, the system ensures that all data remains private, as it is transmitted directly between devices over a peer to peer connection without passing through a centralised servers.

**The key aims of the project focus on the following aspects:**
1.	**Functionality:** Allow users to securely create and manage a Personal Area Network (PAN) and enable communication within the network via text, voice, video and file sharing between trusted devices.
2.	**Privacy:** No personal information is required to use the application. The communication remains completely peer to peer, ensuring no data is stored on external servers.
3.	**Universal Accessibility:** A no app based system that is available to all digital devices given they have a web browser, removing the need for software installation and making the platform easily and widely accessible.
4.	**Enhanced Usability:** A user friendly interface that focuses on simple navigation and allowing the functionality to be performed effortlessly, addressing common frustrations with other third-party applications.

By focusing on these aims the project was able to provide a comprehensive, privacy focused and accessible solution to many of the complexities of modern communication systems.

## Project Features
#### Personal Area Network Creation and Management:
- **Dynamic Creation:** Users can easily create a Personal Area Network (PAN) by adding multiple devices into single group. This allows the added devices to securely communicate via peer to peer connections between the devices.
- **Customised PAN Names and Device Names:** PAN names are randomly generated upon creation but, users have the option to assign custom names to both the Personal Area Network (PAN) and each connected device, improving usability and identification of trusted devices. Users can also specify the device type (desktop, laptop, tablet or mobile) to provide additional clarity for device management.
- **Group Leaders and Management:** Each PAN has one device that is assigned as the leader, where the user can manage device connections and permissions. The leader has the authority to approve or reject new devices, as well as remove unwanted devices and transfer leadership.
- **Scalable:** The system is designed to support the addition of many devices to the PAN, allowing for flexible and scalable use, without performance degradation.

#### Real Time Peer To Peer Communication:
- **Voice, Video, and Text Based Communication:** The platform supports secure, real time peer to peer communication between devices, including voice and video calls, as well as text-based messaging. Users can engage in both one on one and group conversations within the PAN.
- **Direct Peer To Peer Connections:** WebRTC is used to establish direct communication links between devices, bypassing the need for a central server and ensuring fast, private communication. Video and voice calls are sent using WebRTC media streams and text based messages use WebRTC data channels.

#### File Sharing:
- **File Transfers:** Users can securely share files and media directly with other devices in the PAN via WebRTC data channels, ensuring that all transfers are peer-to-peer and remain private.
- **Support for Large Files:** The project supports the transfer of large files by dividing them into smaller chunks for efficient and reliable transmission.

#### Interface:
- **Intuitive, User Friendly Design:** The interface is designed to be clean and easy to navigate, prioritising usability. Key features such as text, video, and file sharing options are easy to access through easy to find menus.
- **Dynamic User Feedback:** When a new device attempts to join a PAN, the system provides clear, on screen notifications to the PAN leader, allowing them to promptly accept or reject the request.
- **Real Time Updates Reflected On Connected Devices:** Changes such as new device connections or change in media streams are reflected in real time across connected devices.
- **Device Recognition and Display:** Each device is represented with a custom device type icon and name, making it easier for users to manage their personal area network. This visual identification ensures the users can clearly see which device is performing specific actions within the PAN.
- **Collapsible and Adaptive Design Elements:** Elements such as video streams and chat windows can be collapsed or expanded according to user preferences, providing flexibility and ensuring the best experience regardless of the device being used.

#### No App Based System:
- **Browser Based Solution:** This project provides a fully browser based solution that eliminates the need for any additional software installation or third party applications. This ensures universal accessibility across all devices that can run a modern web browser and therefore, simplifying the user experience and reducing common security risks commonly associated with third-party applications.

#### Privacy and Security:
- End-to-End Encryption: WebRTC’s built-in encryption ensures that all voice, video, and data streams are fully protected from interception, safeguarding communications across peer to peer connections.
- No Data Stored or Passed Through Centralised Servers: The system operates on a peer to peer architecture when communicating with other devices, meaning that no personal information, communication logs, or media files are stored or pass through external servers, keeping user data private and secure.
- No App Downloads Required: Users can access the platform directly through their web browser, without the need to download or install any third-party applications, reducing common security risks associated with software installations.
- No Personal Data Required: The system does not require users to input any personal data to make use of its functionalities, maintaining privacy and ensuring that no sensitive information is shared or stored.


## System Architecture



## Demo
Here is a demonstration of using the Do You Expect Me To Talk? project where multiple devices (desktop, laptop and mobile) join a Personal Area Network (PAN) and interact over WebRTC peer to peer connections through text messaging, file sharing and real time video calls.
<p align="center">
    <iframe width="854" height="480" src="https://www.youtube.com/embed/6wUoPsU0N2Q?si=BgbIMbSAhIHeGntG" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
</p>

## Conclusion
