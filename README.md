<h1> 🌐 Simulated Cyber Attack & Detection – Cisco Packet Tracer </h1>

 

<h2>Description</h2>
This project simulates a cyber attack and defensive response within a segmented network environment using Cisco Packet Tracer. The lab demonstrates network reconnaissance (port scanning) and basic DoS attack attempts from an attacker PC. Defensive mechanisms include VLAN segmentation, Router-on-a-Stick inter-VLAN routing, and Access Control Lists (ACLs) configured on the router to block unauthorized traffic. The goal was to apply real world network security concepts by isolating the attacker and preventing access to critical systems like the web server.
<br />


<h2>Utilities Used</h2>

- <b> Cisco Packet Tracer (network simulation) </b>
- <b> Telnet (manual port scanning simulation)</b>
- <b> ICMP (ping for DoS simulation)</b>
- <b> Access Control Lists (ACLs) for traffic filtering</b>
- <b> VLAN segmentation for network isolation</b> 
- <b> Router-on-a-Stick (sub-interfaces with 802.1Q trunking) </b>

<h2>Environments Used </h2>

- <b> Cisco 2911 Router </b>
- <b> Cisco 2960 Switch </b>
- <b> 2 Legitimate PCs (Client VLAN) </b>
- <b> 1 Web Server (Server VLAN) </b>
- <b> 1 Attacker PC (Isolated Attacker VLAN) </b>

<h2>Project Documentation & Walkthrough </h2>




<p align="center">
Initial Setup <br/>
<img src="https://i.imgur.com/iq0VCfo.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Request time out after impementing ACL on VLANs <br/>
<img src="https://i.imgur.com/EHo0rn8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

  
<h2> ✅ Conclusion</h2>
This lab successfully demonstrated the use of network segmentation and access control techniques to protect critical assets from unauthorized access within a simulated network environment. By isolating the attacker in a separate VLAN and enforcing ACLs on the router, malicious traffic was effectively blocked while allowing legitimate inter-VLAN communication. This project reinforced key networking and security concepts, including VLAN management, router configuration, ACL implementation, and basic attack simulation techniques.
<br />





































<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
