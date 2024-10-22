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

__1. Adding AD Domain Services and Post Deployment Configuration__ <br/>
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
<br/> 
<br/>
The account is now in both Users and Admins groups
<img src="https://github.com/henrykim-projects/activedirectory_config/blob/c6a8cd48df4631062bc775b02b18d89e1df486c4/images/nc_18.PNG" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br/>
__2. Adding Routing and Remote Access__ <br/>
<br/>
a. In "Add Server Roles", select Remote Access: <br/>
<img src="https://github.com/henrykim-projects/activedirectory_config/blob/fb1fd1b9678440ccd11c9a9ef883e3d27979df78/images/nc_19.PNG" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br/> 
<br/>
b. We will configure NAT to connect users to the internet through one IP address: <br/>
<img src="https://github.com/henrykim-projects/activedirectory_config/blob/fb1fd1b9678440ccd11c9a9ef883e3d27979df78/images/nc_20.PNG" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br/> 
<br/>
<img src="https://github.com/henrykim-projects/activedirectory_config/blob/fb1fd1b9678440ccd11c9a9ef883e3d27979df78/images/nc_21.PNG" height="50%" width="50%" alt="Disk Sanitization Steps"/>

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
