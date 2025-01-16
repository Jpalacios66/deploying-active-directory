<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Use Server manager to install Active Directory
- Promote dc-1 to Domain Controller
- Add new Orgizational Units to ACtive Directory
- Create a New User
- Add New User to Group
- Join Client1 to domain

<h2>Deployment and Configuration Steps</h2>

<p>
<img src="1AD.png" height="80%" width="80%" 
</p>
<p>
Log into dc-1 and go to Server Manager and click add features. Click next through the first 3 tabs and when you get to Server roles check the box that is marked Active DIrectory Domain Features. Click next through the next 2 tabs and when you get to Confirmation select the box that says restart if neccesarry and click yes then press install.
</p>
<br />

<p>
<img src="StaticIP.png" height="80%" width="80%" 
</p>
<p>
Go back to dc-1 and go back to server manager on the right corner click the flag and select "Promote this server to a domain controller". Click next on the next 4 tabs and select Install. It should restart on its own after it has been installed.
</p>
<br />

<p>
<img src="VirtualMachines.png" height="80%" width="80%" 
</p>
<p>
Log back in to dc-1 (make sure to login as a domain user)
</p>
<br />
<p>
<img src="DNS.png" height="80%" width="80%"
</p>
<p>
Go to Active Directory Users and Computers right click mydomain.com and add New Origzational Unit (_EMPLOYEES,_ADMINS)
</p>
<br />
<p>
<img src="ResourceGroup.png" height="80%" width="80%" 
</p>
<p>
Create a new employee. 
Go to _ADMIN and right click folder and go to new then user, and create new user.
</p>
<br />
<p>
<img src="ResourceGroup.png" height="80%" width="80%" 
</p>
<p>
Add new user to _ADMIN
Right click Jane and go to properties. Go to member of and select add. Type admin domain and check names. Add the new user to that group and select apply then ok.
Log off and log back in as the new user
</p>
<br />
<img src="Client1.png" height="80%" width="80%" 
</p>
<p>
Join Client1 to domain
Log into Client1 and Right click the start and click system Then scroll down to Rename this PC(advanced) then cick change
</p>
<br />
