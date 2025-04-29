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
Configured the network layout with a router, switch, two legitimate PCs, a web server, and an attacker PC. All devices were properly cabled using straight-through Ethernet connections. <br/>
<img src="https://i.imgur.com/iq0VCfo.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Created separate VLANs for different device groups. <br/>
<img src="https://i.imgur.com/sPOIhxA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
After creating and assigning VLANs, verified the VLAN configuration on the switch to ensure all devices were correctly segmented. <br/>
<img src="https://i.imgur.com/30eKtVK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Set up sub-interfaces on the router's physical interface with 802.1Q encapsulation for each VLAN. Enabled inter-VLAN routing by assigning gateway IPs for each VLAN subnet. <br/>
<img src="https://i.imgur.com/zW1Up2O.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Configured the switch port connected to the router (GigabitEthernet0/1) as a trunk port using 802.1Q encapsulation. This allows VLAN-tagged traffic from all defined VLANs (10, 20, 30) to be carried across the trunk link to the router. <br/>
<img src="https://i.imgur.com/5zCbJvE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Manually configured static IP addresses, subnet masks, and default gateways on each device to align with the VLAN structure and router sub-interface addresses. <br/>
<img src="https://i.imgur.com/PDfBBix.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Manually configured static IP addresses, subnet masks, and default gateways on each device to align with the VLAN structure and router sub-interface addresses part 2. <br/>
<img src="https://i.imgur.com/Kc8m6DD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Verified basic network connectivity by pinging between devices across VLANs, ensuring legitimate PCs could reach the web server and each other through the router. <br/>
<img src="https://i.imgur.com/xmJUAf2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
In the attacker PC; Conducted manual port scanning using Telnet to discover open services on the web server. We can see that insecure ports such as FTP and HTTP are allowed. <br/>
<img src="https://i.imgur.com/93a8pB0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
In the attacker PC; Simulated basic DoS behavior by manually sending repeated ICMP ping requests.  <br/>
<img src="https://i.imgur.com/9R4BAqR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Enable switchport security <br/>
<img src="https://i.imgur.com/ToxB6tB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Created an extended Access Control List (ACL) to specifically block the attacker PC’s IP address from reaching any destination. Applied the ACL inbound on the router’s trunk link interface. <br/>
<img src="https://i.imgur.com/y8fckyI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Request time out after impementing ACL on VLANs <br/>
<img src="https://i.imgur.com/cK6SDRE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
