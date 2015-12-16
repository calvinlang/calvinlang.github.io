--- 
published: true
title: Web Security and the SSL HandShake
layout: post
author: Calvin
categories: [Software Development]

---


We’ve all seen the Secure Sockets Layer (SSL) certificates that show up when we are logging into a web site. Most notable is you have seen “Verisign” on a web site you’ve visited. This let’s us know that it is a verified and secure site and the SSL protocols encrypt the data that transfers between your own client computer and the servers protecting your private information. So your credit cards, address and other personal information are encrypted between you and the server. One part of this is the initial interaction, also known as the “handshake.” Let’s talk about what happens during this process.

First of all, this is an interaction between the you the client and the server.

When you log in to a site your client computer sends a hello that includes a key exchange message, a cypher, and a hash.

- Key - method of cryptography your client chooses
- Cypher - a cypher that lists its available authentication, encryption, message authentication code (MAC) and exchange algorithms used to negotiate the security settings
- Hash - A unique message authentication code
- Then on the server side it will send the client it certification’s serial number, the issuer (like Versign) and its public key.

At this point the client computer starts encrypting. A master secret code is generated with a cypher spec. The server then also respond with a cypher spec. After this all messages are now encrypted based on the agreed specifications.

This way when you send your credit card expiration of "10/19" it may send off something as elaborate as s$38f"gHU**S that the server will receive and interpret as “10/19."