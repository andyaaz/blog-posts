---
title: "Networking Basics"
description: "Networking Basics"
slug: "networking-basics"
createdAt: "2021-02-15"
tags: ["networking"]
---

OSI (Open Systems Interconnection model)

1. Application layer (e.g. HTTP, SSH, SSL/TLS)

- **why**: top level APIs, application networking. programmer's layer

2. Presentation layer (e.g. MIME)

- **why**: makes sure data is readable why application layer of the receiver

3. Sessoin layer (e.g. RPC)
4. Transport layer (e.g. TCP, UDP)

- **why**: to have flow control. With TCP, sequence and completeness of packets can be ensured (by having a segment with which a connection can be established). UDP allows faster data transmission.

5. Network layer (e.g. IP)

- **why**: to uniquely identify devices in the world, give them IP addresses. a new frame will be created when packets are transmitted from device to another device till it reaches the destined IP address.
- **problem**: no way to enforce packets sequence and whether packets are delivered not not (if needed).
- what is trahsferred: packet (wrapped in a frame)
- example device: router (forwarding packets, unwrap frame and wrap packet in a new frame)
- need to use ARP to get MAC address with IP address (in order to create he frame)

6. Data link layer (e.g. ARP)

- **why**: to solve collision problem by adding source and destination MAC addresses to frame so that at most two devices send data at the exact same time can collide. also can detect if there's a carrier if one is sending data to another.
- **problem**: works only for local network. can't communicate across the globe.
- what is transmitted: frame (in form of bits)
- example device: switch (smart hub with layer 2 capability)

7. Physical layer

- **why**: to transfer physical bits
- **problem**: 1 on 1 is ok. For multiple devices, hub can only boardcast data to all connected devices thus increase chance of collision.
- what is transmitted: bit
- example device: hub

Subnetting

- CIDR ~= subnet masks
  - 255.255.255.0 ~= 123.123.2.0/24
    - 255.255.255 is network prefix (24 bits)
    - 0 is host identifier (8 bits)
- use dot decimal notation
