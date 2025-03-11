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

<h1> Deploying Active Directory</h1>

<h2>Install Active Directory</h2>

Login to DC-1 <br/>
Click Add Roles and Features <br/>

![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/3.1%20add%20roles%20and%20features.PNG)
<br />
<br />
Select Server from server pool  <br/>

![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/3.2%20server%20selection.PNG)
<br />
<br />
In Select Server Roles, click Active Directory Domain Services <br/>

![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/3.3%20active%20directory%20domain%20services.PNG)
<br />
<br />
Add Features  <br/>

![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/3.4%20add%20features.PNG)
<br />
<br />
Notice Acitve Directory Domain Services is checked <br/>

![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/3.5%20ad%20domain%20services%20checked.PNG)
<br />
<br />
Check Restart the destination server automatically if required. Click Yes for warning.  <br/>
Click Install <br/>

![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/3.6%20restart%20destination%20server%20if%20required.PNG)
<br />
<br />
Installing...  <br/>

![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/3.7%20installation%20progress.PNG)
<br />
<br />
Click on yellow warning triagle <br/>
Click Promote this server to a domain controller<br/>

![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/4.1%20promote%20server%20to%20a%20dm.PNG)
<br />
<br />
Deployment Configuration<br/>
Select Add a new forest for deployment operation<br/>
For root domain name, type "mydomain.com"<br/>

![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/4.2%20add%20new%20forest.PNG)
<br />
<br />
Ensure DNS server is checked <br/>
Create password  <br/>

![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/4.3%20dc%20options.PNG)
<br />
<br />
DNS Options  <br/>

![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/4.4%20dns%20options.PNG)
<br />
<br />
Click Install  <br/>

![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/4.5%20install.PNG)
<br />
<br />
The DC-1 VM is starting<br/>

![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/5.1%20restarting.PNG)
<br />
<br />
Connect to DC-1 via remote connection as user: mydomain.com\labuser <br/>

![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/5.2%20rdp%20into%20dc.PNG)
<br />

<h2>Create a Domain Admin user within the domain</h2>

Go to Active Directory Users and Computers (ADUC)  <br/>
Right click "mydomain.com" -> New -> Organizational Unit <br/>

![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/6.1%20aduc%20create%20ou.png)
<br />
<br />
Create an Organizational Unit named _EMPLOYEES <br/>
Create an Organization Unit named _ADMINS  <br/>

![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/6.2%20ou%20employees.PNG)
<br />
<br />
Right click our new _ADMINS folder -> New -> User<br/>

![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/6.4%20new%20user%20janeadmin.png)
<br />
<br />
Create a new employee named “Jane Doe” (same password) with the username of “jane_admin”   <br/>

![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/6.5%20janeadmin.PNG)
![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/6.6%20create%20password.PNG)
![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/6.7%20finish.PNG)
<br />
<br />
<h3>Add jane_admin to the “Domain Admins” Security Group</h3>

Notice Jane Doe as a user in the _ADMINS folder  <br/>
Right click on Jane Doe -> Properties <br/>

![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/7.1%20add%20jane%20to%20jane%20admins%20security%20group.PNG)
<br />
<br />
Go to Member of tab, see she is a member of Domain Users <br/>
Click Add  <br/>

![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/7.2%20member%20of%20add.PNG)
<br />
<br />
Type Domain Admins in the object names <br/>
Click OK <br/>

![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/7.3%20add%20domain%20admins.PNG)
<br />
<br />
See that Jane Doe is a member of Domain Admins and Domain Users <br/>

![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/7.4%20apply%20ok.PNG)
<br />
<br />
Log out of remote connection to DC-1  <br/>
Log back in as “mydomain.com\jane_admin” <br/>
User jane_admin as your admin account from now on <br/>

![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/8.1%20log%20in%20as%20janeadmin.PNG)
<br />

<h2>Join CLIENT-1 to your domain (mydomain.com)</h2>

Login to CLIENT-1 as the original local admin (labuser) <br/>
We need to go to Settings to add the domain to CLIENT-1
Click on System

![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/9.1%20client%201%20settings%20system.PNG)
<br />
<br />
Click About  <br/>

![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/9.2%20about.png)
<br />
<br />
Click Rename this PC (advanced) <br/>

![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/9.3%20rename%20this%20pc.PNG)
<br />
<br />
Click Change  <br/>

![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/9.4%20computer%20name%20change.PNG)
<br />
<br />
Ensure Domain is selected Member of  <br/>
Enter "mydomain.com"
Click OK

![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/9.5%20mydomain.PNG)
<br />
<br />
Enter admin credentials for mydomain.com  <br/>

![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/9.6%20admin%20credentials.PNG)
<br />
<br />
Success  <br/>

![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/9.7%20welcome%20to%20domain.PNG)
<br />
<br />
CLIENT-1 computer will restart  <br/>

![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/9.8%20restart.PNG)
![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/9.9%20restart%20now.PNG)
<br />
<br />

When CLIENT-1 restarts, go into Active Directory Users and Computers (ADUC) <br/>
Open Computers folder and notice CLIENT-1 shows up in ADUC

![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/10.1%20client%201%20is%20in%20aduc.PNG)
<br />
<br />
Create a new OU named “_CLIENTS” and drag Client-1 into there  <br/>

![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/11.1%20create%20ou%20clients.png)
![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/11.2%20create%20client%20ou.PNG)
<br />

<h2>Setup Remote Desktop for non-administrative users on Client-1</h2>

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

