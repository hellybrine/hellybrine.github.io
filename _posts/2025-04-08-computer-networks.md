---
layout:     post
title:      "How do you get Internet?"
subtitle:   " \"Back to Basics\""
date:       2025-04-09 03:46:00
author:     "Mac"
header-img: "img/in-post/internet.jpg"
catalog: true
tags:
    - Networking
    - Fundamentals
---

> "A core component"

## An Introduction

A network is an **interconnected collection of autonomous computers that are connected by a single technology.** Pretty vague, right? Well, that's just networking being mysterious. Now let’s talk about the internet. There’s no one-size-fits-all definition for it. It could be:
- A network of networks
- A collection of routers playing hot potato with your packets
- A global spaghetti of cables that occasionally get bitten by sharks

And honestly, all of them are valid. The first real attempt at computer networking was in the 1960s when the US Department of Defense got bored and built ARPA, which stands for Advanced Research Projects Agency. Their goal? To let UCLA, UCSB, Stanford, and Utah chat without needing carrier pigeons. The result was ARPANET, the grandfather of today’s internet. It also gave us TCP/IP, which now makes your memes and cat videos go from one part of the world to another.

If you zoom out and look at how India gets its internet, you’ll find something cool. All our internet enters through a few coastal cities, mainly Mumbai and Chennai. These are called **Network Access Points (NAPs)**. Imagine a bunch of Kevlar-coated fiber optic cables rising from the ocean like high-speed seaweed. These NAPs connect to **National ISPs**, which then fan out to **Regional ISPs** and finally your **Local ISP**, which may or may not throttle your speed after 1 AM.

Now, when your computer tries to connect to the web, it doesn't just scream into the void. It sends signals, but they’re analog. To get these where they need to go, they travel through **Points of Presence (POPs)**, which are basically clusters of routers set up by the ISP. These POPs are connected to something called the **backbone**, which is the ultra-high-speed highway of the internet, not to be confused with your backbone which has much less bandwidth.

There’s often confusion between **wireless** and **mobile** networks. Wireless (Wi-Fi) uses the 802.11 standards and operates within a limited range like your home or coffee shop. Mobile networks, on the other hand, are based on cellular technology and operate on broader frequencies, enabling you to scroll reels while stuck in traffic.

## Transmission Technologies

Let’s talk about how we move data around. We’ve got two major styles here:

1. **Broadcast Networks**: One sender, many receivers. Think of it like yelling in a room. Ethernet and Wi-Fi often work this way, where everyone hears everything and decides if it’s meant for them.

2. **Point-to-Point Networks**: One-to-one connections. More like whispering into someone’s ear. Used in most backbone and ISP-level connections.

Switching comes in two delicious flavors:

- **Circuit Switching**: Like booking a whole road just for yourself. Great for old-school phones, but a bit wasteful for data.
- **Packet Switching**: Chop your data into pieces, slap on an address, and send it out. The internet loves this style because it’s way more efficient and lets multiple people use the same road at once.

## Network Types

We have all shapes and sizes of networks:

- **LAN (Local Area Network)**: Your home, office, or university. Short range, high speed.
- **MAN (Metropolitan Area Network)**: Think city-wide. Often used for infrastructure, campuses, or ISPs.
- **WAN (Wide Area Network)**: Covers a large geographical area. The internet is the grandest WAN of them all.

Also, based on usage style, networks can be:

- **Peer-to-Peer (P2P)**: Everyone shares and contributes. Like a potluck dinner, but with files.
- **Client-Server**: One boss (the server) and many minions (clients). Netflix is your server. You're the client binge-watching at 2 AM.

## Reference Models

When people say "let’s follow the model," they usually mean either of these two:

### The OSI Model (Our Star Icon)

Seven-layer cake of networking:
1. **Physical**: Wires, cables, voltages.
2. **Data Link**: Framing, error detection. Say hi to MAC addresses.
3. **Network**: Routing and IP addresses.
4. **Transport**: Reliable delivery. TCP and UDP live here.
5. **Session**: Manages sessions. Not always visible.
6. **Presentation**: Formatting, encryption.
7. **Application**: Where you live, with your browser, mail client, etc.

### TCP/IP Model

The cool kid that actually gets used. It has four layers:
- **Link**
- **Internet**
- **Transport**
- **Application**

Think of it as a slightly more efficient remix of the OSI model. TCP/IP is what runs the internet in real life.

## Topology

How we connect stuff matters. There’s a variety of ways:

- **Bus**: One big wire. If it breaks, everyone cries.
- **Star**: One central hub. Popular and easy to manage.
- **Ring**: Like passing a message around a circle. Old but gold.
- **Mesh**: Everyone is connected to everyone else. Great for reliability.
- **Hybrid**: A mix of all of the above. Because why not.

## Protocols and Standards

We follow protocols not just in parties but in networking too. Some common ones include:
- **HTTP**: Web browsing
- **FTP**: File transfers
- **SMTP**: Emails
- **DNS**: Name to IP translation

These are standardized by organizations like **ISO**, **IEEE**, and **IETF** so your router and my router can be besties.

## Conclusion

From physical wires under oceans to high-level protocols negotiating your YouTube binge session, networking is magic, science, and a bit of chaos. The next time your internet goes down, just remember there's a non-zero chance a fish somewhere nudged a cable and now your router is panicking. It's all connected.




