<h1>Active Directory Home Lab</h1>

 

<h2>Description</h2>
Creation of an Active Directory through VirtualBox with the use of a Windows Server 2022 Virtual Machine, as well as adding a user to the 
Active Directory through use of a Windows 10 Enterprise Virtual Machine
<br />


<h2>Utilities Used</h2>

- <b>VirtualBox</b> 
- <b>Windows Server 2022 Virtual Machine</b>
- <b>Windows 10 Enterprise Virtual Machine</b> 
<h2>Environments Used </h2>

- <b>Windows 10</b>
- <b>Windows Server 2022</b>
<h2>Walk-through:</h2>

<p align="center">
Launch VirtualBox and install the Windows Server 2022 VM & Windows 10 Enterprise VM (Ignore the Kali VM) <br/>
<img src="https://i.imgur.com/HUQVoYW.png"height="80%" width="80%" alt=""/>
<br />
<br />
Launch both VM's and follow the Windows Setup and select Custom for both machines:  <br/>
<img src="https://i.imgur.com/lLXTHQU.jpg" height="80%" width="80%" alt=""/>
<br />
<br />
Configure a Virtual Network by going to File > Tools > Network Manager and then NAT Networks and apply. Do this for both VM's by right-clicking on each one  <br/>
<img src="https://i.imgur.com/us3sOKn.png" height="80%" width="80%" alt=""/>
<br />
<br />
On the Windows 10 machine head to Network Connections Ethernet > Properties > IPV4 selection and click on properties
  and insert the IPV4 Address of the 2022 server machine into the DNS box on the Windows 10 machine:  <br/>
<img src="https://i.imgur.com/ANoyNBb.png" height="80%" width="80%" alt="s"/>
<br />  <br/>
  Inside the Windows Server 2022 head to the Server Manager and click Add roles and features, proceed to Server Roles and  click on "Active Directory Domain Services", confirm and install
<img src="https://i.imgur.com/JiYCZgL.png" height="80%" width="80%" alt=""/>
<br />
<br />
Click the flag on the top right corner and click "Promote this server to a domain controller"  <br/>
<img src="https://i.imgur.com/3iHlQR2.png" height="80%" width="80%" alt="s"/>
<br />
<br />
Select "Add a new forest" and name it "iron.local", proceed to create a password for the DSRM and verify the NetBios domain name  <br/>
<img src="https://i.imgur.com/90cafyP.png" height="80%" width="80%" alt=""/>
<br />
<br />
Select "Tools" and proceed to "Active Directory Users and Computers" click "iron.local" then "Users" right click and select New > User
<img src="https://i.imgur.com/0IywmhR.png" height="80%" width="80%" alt=""/>
<br />
<br />
On the Windows 10 machine search for "Access work or school" and join the "iron.local" domain, insert the user information
 <img src="https://i.imgur.com/jbD3g9p.png" height="80%" width="80%" alt=""/>"
<br />
<br />
Active Directory is setup and ready for more users to be added!




</p>


<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
