<h1>Active Directory: Creating Virtual Machines and Installing Server 2019</h1>


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
<img src="https://github.com/henrykim-projects/activedirectory_config/blob/8145d25f7512cb302bc680d3de4bd4ccc6676812/images/nc_2.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://github.com/henrykim-projects/activedirectory_config/blob/8145d25f7512cb302bc680d3de4bd4ccc6676812/images/nc_1.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
b. Allocate the appropriate RAM and CPU cores:  <br/>
<img src="https://github.com/henrykim-projects/activedirectory_setup/blob/30e3c09a26f35254b2a7c6c866a2f4e5d0d049b8/images/dc_2.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br/>
<br />
c. Allocate the amount of storage, 20 GB is plenty: <br/>
<img src="https://github.com/henrykim-projects/activedirectory_setup/blob/56c144161a565f567c4c592d103c814d6026bc34/images/dc_3.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br/>
d. Along with Adapter 1 'NAT' that is turned on by default, enable Adapter 2 as an interal network: <br/>
<img src="https://github.com/henrykim-projects/activedirectory_setup/blob/90be8d8a94e768dd13fbd97e420f837f43bc129a/images/dc_6.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br/>
__2. Installing Server 2019__ <br/>
<br/>
a. Turn on the VM and boot the Server iso.:
<img src="https://github.com/henrykim-projects/activedirectory_setup/blob/7cca62df74893d64752e848328e66cf789d87fa9/images/dc_7.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br /> 
<br/>
b. Select the Standard Desktop Experience for GUI and ease of use: <br/>
<img src="https://github.com/henrykim-projects/activedirectory_setup/blob/7cca62df74893d64752e848328e66cf789d87fa9/images/dc_8.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />  
<br />
c. Set a password for the admin account:  <br/>
<img src="https://github.com/henrykim-projects/activedirectory_setup/blob/7cca62df74893d64752e848328e66cf789d87fa9/images/dc_10.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
d. After successfully logging in, our VM will be ready:  <br/>
<img src="https://github.com/henrykim-projects/activedirectory_setup/blob/7cca62df74893d64752e848328e66cf789d87fa9/images/dc_11.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
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
