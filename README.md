<h1>Active Directory: Domain Services, Remote Access, and DHCP Server Roles Configuration</h1>


<h2>Description</h2>
This project involves creating an internal network with virtual machines. DHCP, NAT, and AD Domain services will be set up to provide users with IP addresses, allowing internet access through the Domain Controller rather than an external connection. A PowerShell script will be used to create a bulk of random user accounts. Successful connectivity will be confirmed by logging into a user account with provided login username and password. 
In this step, we will be configuring the Domain Controller with the protocols necessary to manage the internal network. 
<br/>


<h2>Environments and Technologies Used</h2>

- <b>Active Directory</b>
- <b>Remote Desktop</b>
- <b>Network Configuration</b>

<h2>Environments Used </h2>

- <b>Windows 10</b>
- <b>Server 2019</b>

<h2>Configuration Steps:</h2>

__1. Configuring the Network Adapters and Domain Controller IPv4 Address__ <br/>
</br>
a. Distinguish the internal network from the NAT connection by renaming them. In this case, the NAT connection can be easily discerned by the 10.0.2.15 IP address:
<img src="https://github.com/henrykim-projects/activedirectory_config/blob/8145d25f7512cb302bc680d3de4bd4ccc6676812/images/nc_2.PNG" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<br/>
<img src="https://github.com/henrykim-projects/activedirectory_config/blob/8145d25f7512cb302bc680d3de4bd4ccc6676812/images/nc_1.PNG" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<br />
<br />
b. Provide the IPv4 address for the Domain Controller's internal network adapter:  <br/>
<img src="https://github.com/henrykim-projects/activedirectory_config/blob/b6ec3867b0209eac8bf82a9a2fdc9fce8d73639e/images/nc_4.PNG" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<br/>
<br />
Here, we have manually configured the IP address, subnet mask, and DNS server. Because the Domain Controller will be using itself as the DNS server, the loop back address '127.0.0.1' is used: <br/>
<img src="https://github.com/henrykim-projects/activedirectory_config/blob/b6ec3867b0209eac8bf82a9a2fdc9fce8d73639e/images/nc_5.PNG" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<br />
<br/>

__2. Adding AD Domain Services and Post Deployment Configuration__ <br/>
<br/>
a. Next we will be adding AD Domain Services: <br/>
<img src="https://github.com/henrykim-projects/activedirectory_config/blob/888ec3e102923dc668412a4d4668d7b0429c636f/images/nc_6.PNG" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br/> 
<br/>
b. Post-deployment configuration: <br/>
<img src="https://github.com/henrykim-projects/activedirectory_config/blob/7d2b6b00db83259673f2465f2696081894db7a65/images/nc_8.PNG" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<br />  
<br />
c. Creating the main domain forest:  <br/>
<img src="https://github.com/henrykim-projects/activedirectory_config/blob/7d2b6b00db83259673f2465f2696081894db7a65/images/nc_9.PNG" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<br />
<br />
d. After successfully completeing configuration, the domain name and admin account will be visible:  <br/>
<img src="https://github.com/henrykim-projects/activedirectory_config/blob/7d2b6b00db83259673f2465f2696081894db7a65/images/nc_11.PNG" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<br />
<br />
e. With AD Users and Computers, create a organizational unit for admin accounts: <br/>
<img src="https://github.com/henrykim-projects/activedirectory_config/blob/25b2e12ea93c1007e18c14c32d4346ab17dfd628/images/nc_13.PNG" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br/> 
<br/>
f. Create admin account. Password expiration and change password settings add layers of account management: <br/>
<img src="https://github.com/henrykim-projects/activedirectory_config/blob/25b2e12ea93c1007e18c14c32d4346ab17dfd628/images/nc_15.PNG" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br/> 
<br/>
<img src="https://github.com/henrykim-projects/activedirectory_config/blob/25b2e12ea93c1007e18c14c32d4346ab17dfd628/images/nc_16.PNG" height="50%" width="50%" alt="Disk Sanitization Steps"/>

</p>

<h2>Final Thoughts</h2>
With the Domain Controller set up on a VM connected to the internal network, it is now possible to configure AD services and other networking protocols to set up our network. This was great hands-on experience that demonstrates concepts in network configuration, remmote desktop, and virtual machines. Next we will be providing users with internet access by a DHCP provided IP address.
<br><br/>
<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
