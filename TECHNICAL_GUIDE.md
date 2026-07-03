# Technical Setup Guide

## 1. Virtual Machine Configuration
| VM | CPU / RAM | Disk Space |
| :--- | :--- | :--- |
| pfSense | 2-Core CPU / 2 GB RAM | 15 GB Disk[cite: 1] |
| Kali Linux | Pre-built VirtualBox Image | N/A[cite: 1] |
| Ubuntu | 2-Core CPU / 2 GB RAM | 20 GB Disk[cite: 1] |

## 2. Network Interface Setup (VirtualBox)
1. **pfSense:** Adapter 1 attached to Bridged, Adapter 2 attached to Internal Network (intnet)[cite: 1].
2. **Kali Linux:** Adapter 1 attached to Bridged[cite: 1].
3. **Ubuntu:** Adapter 1 attached to Internal Network (intnet)[cite: 1].

## 3. pfSense Initial Configuration
1. Access the pfSense console (Option 2) to set the LAN interface IP[cite: 1].
2. Assign the LAN IP to `192.168.1.1` with a `/24` subnet[cite: 1].
3. Enable the DHCP server on the LAN interface with a range of `192.168.1.100` to `192.168.1.199`[cite: 1].
4. Disable IPv6 DHCPD[cite: 1].

## 4. Static Routing Configuration
1. Kali requires a static route to reach the internal LAN network (192.168.1.0/24) via the pfSense WAN IP[cite: 1].
2. Run the following command on Kali: `ip route add 192.168.1.0/24 via 192.168.29.241`[cite: 1].