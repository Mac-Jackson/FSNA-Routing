<p align="center">
<img src="https://i.imgur.com/gYF95Kr.png" alt="Routing Logo"/>
</p>

<h1>Inter-VLAN Routing For 3 VLANs + Default Route To Internet</h1>
This Lab tutorial outlines how to configure, test, and verify Inter VLAN routing.<br />




<h2>Networking Technologies Used</h2>

- Inter-VLAN Routing
- Subnetting


<h2>Environments Used </h2>

- Command-Line Interface (CLI)


<h2>Tools Used </h2>

- Cisco Packet Tracer

<h2>High-Level Deployment and Configuration Steps</h2>

- Step 1  Configure FSNA-RTR with Inter-VLAN routing, DHCP, & Internet Services
- Step 2  Configure Interface G0/0 for Inter-VLAN routing for the Mgmt, Data, & Voice VLANs
- Step 3  Configure DHCP Services for the Data VLAN
- Step 4  Add a Default Route for Internet Access

<h2>Deployment and Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/y91MAJk.png" height="80%" width="80%" alt="FSNA-RTR"/>
</p>
<p>
Connectivity between Switch and Router is Off.
</p>
<br />

<p>
<img src="https://i.imgur.com/jUiZnuy.png" height="80%" width="80%" alt="FSNA-RTR"/>
</p>
<p>
Turn on RTR (config)#interface g0/0
 (config)#no shutdown
 (config)#description Trunk to FSNA-SW1
</p>
<br />

<p>
<img src="https://i.imgur.com/XwEWFF4.png" height="80%" width="80%" alt="FSNA-RTR"/>
</p>
<p>
Configure G0/0Sub-interfaces for Inter-VLAN routing. (config-if)#interface g0/0.100
 (config-subif)#description MGMT
 (config-subif)#encapsulation dot1q 100
 (config-subif)#ip address 192.168.100.1 255.255.255.0
 (config-subif)#ip nat inside
 (config-if)#interface g0/0.200
 (config-subif)#description DATA
 (config-subif)#encapsulation dot1q 200
 (config-subif)#ip address 192.168.200.1 255.255.255.0
 (config-subif)#ip nat inside
 (config-if)#interface g0/0.150
 (config-subif)#description VOICE
 (config-subif)#encapsulation dot1q 150
 (config-subif)#ip address 192.168.150.1 255.255.255.0
 (config-subif)#ip nat inside
</p>
<br />

<p>
<img src="https://i.imgur.com/vmGqwxo.png" height="80%" width="80%" alt="FSNA-RTR"/>
</p>
<p>
Verify the Trunk is active. FSNA-RTR#show running-config
</p>
<br />

<p>
<img src="https://i.imgur.com/91pR34D.png" height="80%" width="80%" alt="FSNA-RTR"/>
</p>
<p>
FSNA-RTR#show ip route
</p>
<br />

<p>
<img src="https://i.imgur.com/dxscWap.png" height="80%" width="80%" alt="FSNA-RTR"/>
</p>
<p>
Save the configuration
</p>
<br />

<p>
<img src="https://i.imgur.com/ViVYP1x.png" height="80%" width="80%" alt="FSNA-SW1"/>
</p>
<p>
Confirm Active Trunk on FSNA-SW1
</p>
<br />

<p>
<img src="https://i.imgur.com/twzgPHn.png" height="80%" width="80%" alt="FSNA-SW1"/>
</p>
<p>
Add a default gateway to the switch and save configuration.
</p>
<br />

<p>
<img src="https://i.imgur.com/8ZDLtQh.png" height="80%" width="80%" alt="FSNA-SW1"/>
</p>
<p>
FSNA-SW1#ping 192.168.100.1
 FSNA-SW1#ping 192.168.200.1
 FSNA-SW1#ping 192.168.150.1
</p>
<br />
