<p align="center">
<img src="https://i.imgur.com/gYF95Kr.png" alt="Routing Logo"/>
</p>

<h1>Inter-VLAN Routing For 3 VLANs + Default Route To Internet</h1>
LAB: ROUTER LAN CONFIGURATION. Configure, Test & Verify Inter-VLAN Routing<br />




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
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
