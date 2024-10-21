<h1>Active Directory: Creating Virtual Machines and Installing Server 2019</h1>


<h2>Description</h2>
This project involves creating an internal network with virtual machines. DHCP, NAT, and AD Domain services will be set up to provide users with IP addresses, allowing internet access through the Domain Controller rather than an external connection. A PowerShell script will be used to create a bulk of random user accounts. Successful connectivity will be confirmed by logging into a user account with provided login username and password. 
In the preliminary setup, we will use Oracle Virtual Box to create a VM and allot the necessary RAM and CPU cores to install Server 2019. This Domain Controller VM will be used to manually configure the internal network in the next step.
<br/>


<h2>Environments and Technologies Used</h2>

- <b>Active Directory</b>
- <b>Oracle Virtual Box</b>
- <b>Virtual Machine Configuration</b>

<h2>Environments Used </h2>

- <b>Windows 10</b>
- <b>Server 2019</b>

<h2>Configuration Steps:</h2>

__1. Creating the Domain Controller__ <br/>
</br>
a. In Virtual Box, create a VM named "DC":
<img src="https://github.com/henrykim-projects/activedirectory_setup/blob/36110ff5676e843ba76b5a4e3311292910214abc/images/dc_1.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
