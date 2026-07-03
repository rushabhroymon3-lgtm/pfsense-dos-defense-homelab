# pfSense DoS Defense Lab 

## Project Overview
This homelab project demonstrates the setup of a pfSense firewall to defend against a simulated Denial of Service (DoS) attack. The lab features an isolated network where an external attacker (Kali Linux) targets an internal victim (Ubuntu Desktop). 

## Key Results
* **Attack Packets Generated:** 1,774,472
* **Wireshark Capture:** 377,654+ packets
* **Attack Packet Rate:** 177,000 pps[cite: 1]
* **Firewall Blocking Rate:** 100%[cite: 1]

## Project Objectives
* Stand up a pfSense firewall in VirtualBox with separate WAN (bridged) and LAN (internal) segments[cite: 1].
* Put Kali Linux on the WAN side to simulate an external attacker[cite: 1].
* Put Ubuntu Desktop on the LAN side as the victim host[cite: 1].
* Demonstrate DoS traffic with hping3 and show it in Wireshark[cite: 1].
* Mitigate the attack using pfSense firewall rules and view the resulting logs[cite: 1].

## Lab Topology
| Device | IP Address | Network Role |
| :--- | :--- | :--- |
| pfSense WAN | 192.168.29.241/24 (DHCP) | Bridged Adapter[cite: 1] |
| pfSense LAN | 192.168.1.1/24 (Static) | Internal Network (intnet)[cite: 1] |
| Kali Linux (Attacker) | 192.168.29.7 | Bridged Adapter[cite: 1] |
| Ubuntu (Victim) | 192.168.1.100/24 (DHCP) | Internal Network (intnet)[cite: 1] |

## Skills Demonstrated
* **Firewall Admin:** pfSense rule creation, rule precedence, stateful filtering, logging, DHCP[cite: 1].
* **Network Architecture:** Multi-zone segmentation, WAN/LAN design, DHCP, DNS, routing[cite: 1].
* **Attack Simulation:** hping3 ICMP flood, traffic generation, attack verification[cite: 1].
* **Traffic Analysis:** Wireshark live capture, packet forensics, protocol analysis[cite: 1].
* **Linux Admin:** Kali & Ubuntu setup, static routing, UFW, CLI networking tools[cite: 1].
* **Virtualization:** VirtualBox VM management, Bridged/Internal adapters, network design[cite: 1].

## Author
Rushabh Roymon | June 27, 2026[cite: 1]