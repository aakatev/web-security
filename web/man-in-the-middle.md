# Man-in-the-Middle (MITM)

## Overview

MITM attack is an attack where the attacker relays communication traffic between two parties. The most common sub-type of the attack is eavesdropping, when the attacker makes a descrete connection with each victim, and makes them believe they are using a private channel for the communications. Meanwhile, the whole flow of the exchange is controlled by the attacker.

## Common Danger Zones

- Unencrypted Wi-Fi access points
- Often used to implement the downgrade attack, so danger zones are similar

## Defenses

#### Most common prevention measures are:

- Make sure to use HTTPS (with the S) when visiting websites, and especially exchanging some sensitive information
- Avoid connecting to public Wi-Fi routers directly, and use virtual private network (VPN) when possible 

#### VPN and Tor

A VPN extends a private network across a public network and enables users to send and receive data across shared or public networks as if their computing devices were directly connected to the private network. 

Tor directs Internet traffic through a free, worldwide, volunteer overlay network consisting of more than seven thousand relays to conceal a user's location and usage from anyone conducting network surveillance or traffic analysis. 

Used independently, both VPN and Tor are excellent security tools. Nevertheless, they both have shortcomings and should be used combined to gain the full potential. Tor over VPN provides the best network encryption and privacy courtesy of the VPN and anonymity courtesy of Tor. Minimizing your exposure and securing your data online is one of the best ways to protect against man-in-the-middle attacks. 

#### Encryption

Some of the encryption you should pay attention to when protecting from the MITM attack:

- End-to-end encryption - covers the channel, and makes it impossible for parties other than the sender and the recipient to read a message
- Device encryption - covers end security weaknesses, i.e. weaknesses of the sending or receiving device

#### Malware Protection

Malware usage is a common way to bypass various types of encryption. The best way to protect against that is to install an antivirus software designed to detect a malware on your device. A software that provides additional network security and firewall protection could further decrease chances of MITM exploits.

---

Go back to the [section page](web/README.md).
