# Firewall Rule Configurations

To simulate the attack and subsequently mitigate it, specific firewall rules were configured on the pfSense WAN interface[cite: 1].

### Rule Precedence Setup
pfSense evaluates rules top-down and stops at the first match[cite: 1]. The blocking rule MUST be placed above the allow rule[cite: 1].

| Priority | Action | Protocol | Source | Destination | Description |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **#1** | **BLOCK** | IPv4 * | 192.168.29.7 | 192.168.1.100/24 | Block Kali DoS (STOPS HERE)[cite: 1] |
| #2 | PASS | IPv4 * | 192.168.29.7 | 192.168.1.100 | Allow Kali to Ubuntu (never reached)[cite: 1] |

### Logging Configurations
Logging was enabled on the Block Rule to ensure forensic evidence was captured during the attack[cite: 1]. 
1. Edit the "Block Kali DoS" rule[cite: 1].
2. Scroll to Extra Options[cite: 1].
3. Check: "Log packets that are handled by this rule"[cite: 1].
