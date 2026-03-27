---
layout: post
title: "1.1 Open Systems Intercommunication"
date: 2026-03-26 12:00:00 -0800
categories:
   - networkengineer
---

The International Organization for Standardization (ISO) developed a reference model called the Open Systems Interconnection (OSI) model to visualize how most network components relate to each other. It separates hardware and software components into seven layers with each performing distinct functions and coordinating for desired end-user needs. Network techs use numerical and descriptive layers synonymously, such as “Layer 1” and “Physical Layer”, so it is key to know which numerical corresponds to the descriptive. The OSI model is advantageous because it is the primary networking diagnostic tool and helps discern the specific part of the network experiencing problems.

Network protocols exchange data in a structured format. Network protocols have two key functions. Addressing to tell where messages should go and Encapsulation to describe how messages should be packaged for transmission with increasingly specific headers. This is analogous to the post office, as the post office uses postal codes (zip codes and PO boxes) to determine where letters should go and different packaging items (letters and boxes) depending on the type of mail.

Networks involve many protocols at OSI layers. For each layer, the two nodes must run at the same protocol for consistency. When messages are sent from one end-user node to another, it goes down the stack of layers from Application (Layer 7) to Physical (Layer 1) of the sender, the data passes across the transmission media, and the message proceeds up from Physical (Layer 1) to Application (Layer 7) on the receiver (Figure 1). The layers of encapsulation formed at each stage, except for the Physical layer, creates the Protocol Data Unit (PDU). The reverse process of encapsulation is decapsulation. Once the PDU reaches the Physical layer at the receiver node, it travels up the OSI model and is decoded.

![Principal Component Analysis](/assets/networkengineer/OpenSystemsIntercommunication.png)
*Figure 1: Visualization of OSI layers and the direction of packet encapsulation for the sender node and decapsulation for the receiver node shown in red arrows. Physical connection for data transfer between sender and receiver nodes shown in green.*
