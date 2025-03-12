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

<h1>Unlocking Accounts, Resetting Passwords, Enabling and Disabling Accounts</h1>

<h2>Configure Group Policy to lockout account</h2>

On DC-1, open Group Policy Management <br/>

![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/14.1%20group%20policy%20management.PNG)
<br />
<br />
Under mydomain.com, right click the Default Domain Policy -> Edit <br/>

![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/14.2%20edit%20default%20domain%20policy.png)
<br />
<br />
Go to Computer Configuration -> Policies -> Window Settings -> Security Settings -> Account Policies -> Account Lockout Policy <br/>
See the policies in place<br/>
Click on Account lockout duration to view properties<br/>

![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/14.3%20expand%20tree.PNG)
<br />
<br />
Make sure Define this policy is checked <br/>
Set account locked out for 30 minutes <br/>
Click Apply, then OK  <br/>

![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/14.4%20account%20lockout%20duration.PNG)
<br />
<br />
Some suggested values are generated  <br/>
Click OK  <br/>

![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/14.5%20suggest%20value%20changes%20ok.PNG)
<br />
<br />
View our current settings now in place  <br/>

![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/14.6%20policy%20settings.PNG)
<br />
<br />
Log in the CLIENT-1 as jane_admin update policy for users br/>

![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/14.7%20login%20client1%20as%20janeadmin.PNG)
<br />
<br />
Update the group policy <br/>
Open the cmd  <br/>
Enter "gpupdate /force" <br/>
Updates successfully<br/>

![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/14.8%20gpupdate%20on%20cmd.PNG)
<br />
<br />
Log in to CLIENT-1 as our random user to test password policy<br/>
When we enter wrong password 6 times it locks us out<br/>

![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/14.8%20failed%20login%20locked.PNG)
<br />
<br />
<h3>Unlock the account</h3>

On DC-1, right click on our locked out user -> Properties  <br/>

![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/13.4%20pick%20random%20user.PNG)
<br />
<br />
Check Unlock Account<br/>
Click Apply and Enter<br/>

![](https://github.com/rbrianshutt/active_directory/blob/main/Active%20Directory%202.0/14.9%20unlock%20account.PNG)
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


