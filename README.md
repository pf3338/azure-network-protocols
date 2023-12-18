<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Creating a resource group 
- Setting up virtual machines, establishing a connection, and streaming data between them
- Setting up Wireshark 
- Observing ICMP (Internet Control Message Protocol), SSH (Secure Shell Protocol), DHCP (Dynamic Host Configuration Protocol), DNS (Domain Name System), and RDP (Remote Desktop Protocol) traffic using Wireshark

<h2>Actions and Observations</h2>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
To start, we create a Resource Group in Azure. We then setup two virtual machines (with one of them running Windows 10 and the other setup with Ubuntu Server 20.04) within the same Resource Group and virtual network.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
From here, we establish a remote desktop connection into one of the VMs and install Wireshark. 
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once the installation is complete, try to ping the second VM using Powershell. Then, run Wireshark and filter for just ICMP traffic. Observe the requests and replies.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After, initiate a perpetual ping to the second VM and observe what happens.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Using the Network Security Group from within the VM that you just pinged, disable all incoming ICMP traffic and observe any changes. Re-enable ICMP traffic and observe changes again. Once complete, stop the ping activity.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
You can also attempt to ping a public website (i.e. www.google.com) and initiate a perpetual ping should you find it necessary. 
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Traffic can be filtered for specific protocols i.e. SSH, RDH, DNS, and ICMP. Filter for each protocol and observe streams as they appear on Wireshark.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
To finish off this project, close your remote desktop connection and delete the resource group and all Virtual Machines within.
</p>
<br />
