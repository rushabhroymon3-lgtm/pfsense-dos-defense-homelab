# pfSense DoS Defense HomeLab 

## Project Overview
This homelab project demonstrates the setup of a pfSense firewall to defend against a simulated Denial of Service (DoS) attack. The lab features an isolated network where an external attacker (Kali Linux) targets an internal victim (Ubuntu VM). 

## 📁 Repository Structure

```
pfsense-dos-defense-lab/
├── README.md                  ← Project overview
├── TECHNICAL_GUIDE.md         ← Step-by-step setup instructions
├── docs/
│   ├── firewall-rules.md      ← Rule configurations
│   └── attack-analysis.md     ← DoS breakdown & findings
├── screenshots/               ← All 24 screenshots
├── configs/
│   └── pfsense-backup.xml     ← Exported pfSense firewall config
└── reports/
    └── portfolio.pdf          ← Full project report
```

## Project Objectives
* Stand up a pfSense firewall in VirtualBox with separate WAN (bridged) and LAN (internal) segments.
* Put Kali Linux on the WAN side to simulate an external attacker.
* Put Ubuntu Desktop on the LAN side as the victim host.
* Demonstrate DoS traffic with hping3 and show it in Wireshark.
* Mitigate the attack using pfSense firewall rules and view the resulting logs.

## Lab Topology
| Device | IP Address | Network Role |
| :--- | :--- | :--- |
| pfSense WAN | 192.168.29.241/24 (DHCP) | Bridged Adapter|
| pfSense LAN | 192.168.1.1/24 (Static) | Internal Network (intnet) |
| Kali Linux (Attacker) | 192.168.29.7 | Bridged Adapter |
| Ubuntu (Victim) | 192.168.1.100/24 (DHCP) | Internal Network (intnet)|

## Key Results
* **Attack Packets Generated:** 1,774,472
* **Wireshark Capture:** 377,654+ packets
* **Attack Packet Rate:** 177,000 pps
* **Firewall Blocking Rate:** 100%

## Skills Demonstrated
* **Firewall Admin:** pfSense rule creation, rule precedence, stateful filtering, logging, DHCP
* **Network Architecture:** Multi-zone segmentation, WAN/LAN design, DHCP, DNS, routing
* **Attack Simulation:** hping3 ICMP flood, traffic generation, attack verification
* **Traffic Analysis:** Wireshark live capture, packet forensics, protocol analysis
* **Linux Admin:** Kali & Ubuntu setup, static routing, UFW, CLI networking tools
* **Virtualization:** VirtualBox VM management, Bridged/Internal adapters, network design

## Author
Rushabh Roymon 
