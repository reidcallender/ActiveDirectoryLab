<h1>Active Directory Home Lab</h1>


<h2>Description</h2>
The purpose of this lab was to set up active directory in a virtual environment in order to gain some experience with this technology and some basic Windows networking in general. This lab utilized two virtual machines which I created using Oracle VirtualBox. The first VM named, "Server2025", served as my domain controller. Server2025 has two network adapters. The first adapter connected to the internet through my router and was assigned an IP address from DHCP. The second adapter acted as an internal network for clients to connect to and access internet through the domain contoller. I used server roles to implement Active Directory, RAS/NAT, and DHCP. I used a powershellscript obtained from Josh Madakor to simulated 1,000 users in the active Directory. I then connected to my second VM titled "client1" to verify that the network had been implemented succesfully and added this device to the domain.   
<br />


<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b> 
- <b>Oracle VirtualBox</b>


<h2>Environments Used </h2>

- <b>Windows Server 2025</b>
- <b>Windows 10 Pro</b>

<h2>Lab walk-through:</h2>


Created both virtual machines and configured both network adapters on Server2025.  <br/>
<br />
![Image](https://github.com/user-attachments/assets/952550fb-a7ca-4bd6-b69b-2a304b27a4f8)
<br />
<br />
Manually configured IP addressing on the internal NIC <br/>
<br />
![Image](https://github.com/user-attachments/assets/25d69f33-9bc2-4bb1-a97b-b1868a55e741)
<br />
<br />
Installed active directory in server roles. Promoted the server to be my domain controller. Created an Administrators OU. Created a user account for myself in Administrators and promoted it to domain admin. <br/>  
<br />
![Image](https://github.com/user-attachments/assets/587e8dc3-dc6d-4184-a326-c619dffd0278)
<br />
<br />
Installed remote access from server roles and enabled routing. Configured NAT so the client will be able to connect to the internet through the domain controller. <br/>
<br />
![Image](https://github.com/user-attachments/assets/6c3e91e9-f6f1-42e3-83c3-5120389e6e9e)
<br />
<br />
Installed DHCP in server roles. Setup the DHCP server and added a scope.  
<br />
![Image](https://github.com/user-attachments/assets/bea349f9-63d7-42d4-9ae5-85bd82c8e43b)
<br />
<br />
Added the default gateway in the scope which clients will use to access the internet. This is the IP for the internal NIC. <br/>
<br />
![Image](https://github.com/user-attachments/assets/93268f56-208a-42a1-8741-c29cec70b290)
<br />
<br />
Used a powershell script to add 1,000 users to Active Directory. This is not my script and was obtained from Josh Madakor at https://github.com/joshmadakor1/AD_PS/blob/master/Generate-Names-Create-Users.ps1. <br/>
<br />
![Image](https://github.com/user-attachments/assets/107322c4-15ef-4c03-ab85-8d975f8902d1)
<br />
<br />
The final result of the script. <br/>
<br />
![Image](https://github.com/user-attachments/assets/1089ceac-2d87-45ca-8a18-0e184712a6ad)
<br />
<br />
Logged into our client1 VM and verified that the network had been succesfully implemented and the client is receiving an IP adress from the DHCP server. <br/>
<br />
![Image](https://github.com/user-attachments/assets/23443f0f-91ba-474f-85f3-1afe61f587c2)
<br />
<br />
Added the client into the domain. <br/>
<br />
![Image](https://github.com/user-attachments/assets/648794e3-4f5b-4f47-a84d-442e48db51ce)

