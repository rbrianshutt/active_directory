<h1>Active Directory</h1>

![]()


<h2>Description</h2>
Lorem ipsum
<br />

<h2>Techonologies Used</h2>

- <b>Microsoft Azure</b> 
- <b>Remote Desktop</b>
- <b>Lorem ipsum</b>

<h2>Program walk-through:</h2>

<h1>Preparing Active Directory Infrastructure in Azure</h1>

<h2>Setup Domain Controller in Azure</h2>

Create a Resource Group  <br/>

![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/1.1%20create%20resource%20group.PNG)
<br />
<br />
Create a Virtual Network and Subnet <br/>

![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/1.2%20create%20virtual%20network.PNG)
<br />
<br />
Create the Domain Controller VM (Windows Server 2022) named “DC-1”  <br/>

![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/1.3%20create%20vm%20dc-1.PNG)
![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/1.3a%20create%20vm%20dc-1.PNG)
<br />
<br />
After VM is created, set Domain Controller’s NIC Private IP address to be static <br/>

![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/1.4%20set%20private%20ip%20nic%20to%20static.PNG)
![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/1.4a%20set%20private%20ip%20nic%20to%20static.PNG)
<br />
<br />
Connect to DC-1 via remote connection <br/>
Log in using credentials <br/>

![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/1.5%20rdp%20into%20dc-1.PNG)
![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/1.5a%20rdp%20into%20dc-1.PNG)
<br />
<br />
Go to Window Defender Firewall  <br/>
Click on Windows Defender Firewall Properties <br/>

![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/1.5b%20disable%20firewall.PNG)
<br />
<br />
Turn Firewall State OFF for the following: <br/>

- <b>Domain Profile</b> 
- <b>Private Profle</b>
- <b>Public Profile</b>

![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/1.5c%20disable%20firewall.PNG)
![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/1.5d%20disable%20firewall.PNG)
![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/1.5e%20disable%20firewall.PNG)
<br />
<br />
Lorem ipsum  <br/>

![]()
<br />
<br />
Lorem ipsum  <br/>

![]()
<br />
<br />
Lorem ipsum  <br/>

![]()
<br />
<br />
Lorem ipsum  <br/>

![]()
<br />
<br />
Lorem ipsum  <br/>

![]()
<br />
<br />
Lorem ipsum  <br/>

![]()
<br />
<br />
Lorem ipsum  <br/>

![]()
<br />
<br />
Lorem ipsum  <br/>

![]()
<br />
<br />
Lorem ipsum  <br/>

![]()
<br />
<br />
Lorem ipsum  <br/>

![]()
<br />
<br />
Lorem ipsum  <br/>

![]()
<br />
<br />
Lorem ipsum  <br/>

![]()
<br />
<br />
Lorem ipsum  <br/>

![]()
<br />
<br />
Lorem ipsum  <br/>

![]()
<br />
<br />
Lorem ipsum  <br/>

![]()
<br />
<br />
Lorem ipsum  <br/>

![]()
<br />
<br />
Lorem ipsum  <br/>

![]()
<br />
<br />
Lorem ipsum  <br/>

![]()
<br />
<br />
Lorem ipsum  <br/>

![]()
<br />
<br />
Lorem ipsum  <br/>

![]()
<br />
<br />
Lorem ipsum  <br/>

![]()
<br />
<br />
Lorem ipsum  <br/>

![]()
<br />
<br />
