I set out to build a functional corporate network for 'Secure Corp' that separates staff from guests. I wanted to move beyond theory and get hands-on with Cisco routing and security policies.

My biggest hurdle was a 4.5-hour troubleshooting session where my pings were successful, but my web browser wouldn't load. After checking my Default Gateways and IP configurations multiple times, I realized I was in Simulation Mode. This taught me that in networking, the 'logic' can be perfect, but you have to understand the 'state' of your tools, the smallest details matter, look closely, be patient and persistent. Moving to Real-Time mode solved it instantly.

# Lab: Secure Corp Network & Security Policy

## 📖 Overview
In this lab, I transitioned from software logic to network infrastructure. I designed a dual-subnet environment using a Cisco Router to bridge a Server Network and an Employee/Guest Network.

## 🛠️ Technical Implementation
1. **Network Topology:** Connected PCs, Laptops, and a Web Server via Cisco Switches to a central Router.
2. **IP Schema:** Configured static IP addresses and Default Gateways to ensure cross-network communication.
3. **Security:** Implemented a Standard Access Control List (ACL) to permit specific employee devices while denying all guest traffic to the internal server.

## 💻 Key Commands Used
```bash
# Assigning an IP to the Router Interface
interface GigabitEthernet0/0
 ip address 192.168.1.1 255.255.255.0
 no shutdown

# Creating the Security Policy (ACL)
access-list 1 permit 192.168.2.10
access-list 1 permit 192.168.2.11
# Note: Implicit deny blocks everyone else!
```


![Network Topology](Topology-Map.png)

![Network Topology](Result-of-Lab.png)
