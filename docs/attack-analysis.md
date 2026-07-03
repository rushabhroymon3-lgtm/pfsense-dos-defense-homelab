# Attack Analysis & Mitigation Breakdown

## Attack Generation
An ICMP flood attack was launched from the Kali Linux host targeting the Ubuntu Desktop[cite: 1].
* **Command Used:** `sudo hping3 -1 --flood 192.168.1.100`[cite: 1]

## Pre-Mitigation Results
Before the block rule was applied, the traffic successfully traversed the firewall[cite: 1].
* **Ping Test:** `ping -c 3 192.168.1.100` resulted in 0% packet loss[cite: 1].
* **Wireshark Capture:** 377,654+ packets were captured in real-time on the Ubuntu host[cite: 1].
* **Total Transmitted:** 1,774,472 packets[cite: 1].

## Post-Mitigation Results
After applying the explicit block rule at the top of the WAN ruleset, the attack was halted[cite: 1].
* **Ping Test:** `ping -c 3 192.168.1.100` resulted in 100% packet loss[cite: 1].
* **Wireshark Capture:** Zero new attack packets arrived from Kali[cite: 1].
* **System Logs:** The "Block Kali DoS" entries were actively recorded in the pfSense Firewall System Logs[cite: 1].
