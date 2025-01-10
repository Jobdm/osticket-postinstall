<p align="center">
<img src="https://i.imgur.com/tuJ3zhI.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10 Pro </b>

<h2>Post-Install Configuration Objectives</h2>

- Login to the osTicket Admin Panel
- Configure Roles
- Configure Departments
- Configure Teams
- Configure Help Topics

<h2>Configuration Steps</h2>
<p> Now that we've built osTicket from scratch we need to configure it. Login to the osTicket Admin Panel. Below is the user interface (UI) where we can view and interact with tickets that are created by the end user.

</p>
<p align="center">
<img src="https://i.imgur.com/lKxYr7c.png" height="65%" width="65%" alt="UI admin/help desk Tickets"/>
</p>

<br />
<details>
 <summary><b>- Configure</b> <a href="https://docs.osticket.com/en/latest/Admin/Agents/Roles.html">[Roles]</a></summary>
 <br /> <b>Here we create a 'Supreme Admin' role. This role is going to have all <a href="https://docs.osticket.com/en/latest/Features/Visibility%20Permissions.html">permissions</a> to perform a wide range of tasks. For this project we will need such a role.</b>
<br/><br/>
<p>Admin Panel -> Agents -> Roles -> Add New Role</p>
<p align="center">
<img src="https://i.imgur.com/KMN2x6E.png" height="65%" width="65%" alt="UI to add Role"/>
</p>
<p>We name the new role: <b>"Supreme Admin"</b></p>
<p align="center">
<img src="https://i.imgur.com/TX3Q6a1.png" height="65%" width="65%" alt="enter role name"/>
</p>
<br />
<p> We enable the permissions for this role.</p>
<p align="center">
<img src="https://i.imgur.com/LEO6fYB.png" height="65%" width="65%" alt="list of permissions"/>
</p>
<br />
<p> Now we have our <b>"Supreme Admin"</b> role.</p>
<p align="center">
<img src="https://i.imgur.com/9J0FpVx.png" height="65%" width="65%" alt="list of permissions"/>
</p>
</details>    
<hr>

<br />
<details>
 <summary><b>- Configure</b> <a href="https://docs.osticket.com/en/latest/Admin/Agents/Departments.html">[Departments]</a></summary><br /> 
 <b>Now we create a 'System Administrator' department to assign our Supreme Admins to.</b>
<br/><br/>
<p>Admin Panel -> Agents -> Departments -> Add New Department</p>
<p align="center">
<img src="https://i.imgur.com/Z7lHE5q.png" height="65%" width="65%" alt="UI to add Role"/>
</p>
<p>Name the new department 'System Administrator' and click `Create Dept`.</p>
<p align="center">
<img src="https://i.imgur.com/mVJTync.png" height="65%" width="65%" alt="enter role name"/>
</p>
</details>    
<hr>

<br />
<details>
 <summary><b>- Configure</b> <a href="https://docs.osticket.com/en/latest/Admin/Agents/Teams.html">[Teams]</a></summary><br />
 <b>Teams allow us to pull agents from various departments and organize them to address specific issues or users. Classic example is 'Level 1/2/3 Support' as each level focuses on different issues and will utilize the best suited agent for those tasks.</b>
<br/><br/>
<p>Admin Panel -> Agents -> Teams -> Add New Team</p>
<p align="center">
<img src="https://i.imgur.com/SRC2E3g.png" height="65%" width="65%" alt="UI to add Role"/>
</p>
<p>Enter a name and click `Create team`.</p>
<p align="center">
<img src="https://i.imgur.com/w8rqerk.png" height="65%" width="65%" alt="enter role name"/>
</p>
<p>The 'Registration Required' setting can be used to help control access to the Help Desk. Users will need to register and login before creating a ticket. For the purposes of this project we will not need it.</p>
<p align="center">
<img src="https://i.imgur.com/XwrVVpQ.png" height="65%" width="65%" alt="enter role name"/>
</p>
</details>    
<hr>

<br />
<details>
 <summary> <b>- Configure</b> <a href="https://docs.osticket.com/en/latest/Admin/Agents/Agents.html">[Agents]</a></summary><br />
 <b>Now we create some agents. Agents are the people that would be working on resolving tickets. They can be assigned to multiple departments and given roles for the departments they're a part of. </b>
<br/><br/>
<p>Admin Panel -> Agents -> Add New Agent</p>
<p align="center">
<img src="https://i.imgur.com/JsrErpV.png" height="65%" width="65%" alt="UI to add Role"/>
</p>
<p>On the 'Account' tab we fill in the name, email, and username. After that we set password. We have a few options available for when we would login, both of which would require us to create a new password. For our case we will leave unchecked.</p>
<p align="center">
<img src="https://i.imgur.com/f5SUAmW.png" height="65%" width="65%" alt="enter role name"/>
</p>
<p>Now we set primary department and primary role for this agent. 'Extended Access' gives the agent additional access to departments where they can take on different roles.</p>
<p align="center">
<img src="https://i.imgur.com/YV6HpGE.png" height="65%" width="65%" alt="enter role name"/>
</p>
</details>    
<hr>

<br />
<details>
 <summary><b>- Configure</b> <a href="https://docs.osticket.com/en/latest/Agent/Users/User%20Directory.html">[Users]</a></summary>  <br />
 <b>Time to get some users in here. These are the people that would be creating tickets for various issues.</b>
<br/><br/>
 <ol><li>Admin Panel -> Users -> Add User</li>
    <li>Fill in Full Name and Email then click Add User</li>
</ol>
<br/>
<p align="center">
<img src="https://i.imgur.com/57TxFWx.png" height="65%" width="65%" alt="UI to add Role"/>
</p>
</details>    
<hr>

<br />
<details>
 <summary><b>- Configure</b> <a href="https://docs.osticket.com/en/latest/Admin/Manage/SLA%20Plans.html">[SLA]</a></summary>  <br />
 <b>We are going to create some SLA plans. Service Level Agreements (SLA) plans provide a guideline for length of time in which the help desk Administrator expects tickets to be closed.</b>
<br/><br/>
 <ol><li>Admin Panel -> Manage -> SLA -> Add New SLA Plan</li>
    <li>Name and Schedule, then click 'Add Plan'</li>
</ol>
<br/>
<p align="center">
<img src="https://i.imgur.com/RrPjKzs.png" height="65%" width="65%" alt="UI to add Role"/>
</p>
<br/>
<p>We created three SLA plans with different 'Grace Period' which is basically a deadline for closing tickets. Grace period hours (hrs) can indicating the severity of an issue, less time meaning urgent and more time meaning not as urgent.</p>
<p align="center">
<img src="https://i.imgur.com/Czge7aX.png" height="65%" width="65%" alt="UI to add Role"/>
</p>
</details>    
<hr>

<br />
<details>
 <summary><b>- Configure</b> <a href="https://docs.osticket.com/en/latest/Admin/Manage/Help%20Topic.html?highlight=help%20topics">[Help Topics]</a></summary>  <br />
 <b>Here we create several help topics. These help end users categorize their tickets, ensuring proper assignment and prompt response.</b>
<br/><br/>
<ol>
<li>Admin Panel -> Manage -> Help Topics -> Add New Help Topic</li>
 <li><ul>We create the following:
        <li> Business Critical Outage </li>
        <li> Personal Computer Issues </li>
        <li> Equipment Request </li>
        <li> Password Reset </li>
</ul></li>
</ol>
<br/>
<p align="center">
<img src="https://i.imgur.com/t9F1ZDV.png" height="65%" width="65%" alt="UI to add Role"/>
</p>
<br/>
<p align="center">
<img src="https://i.imgur.com/SJcmgOW.png" height="65%" width="65%" alt="UI to add Role"/><br/>
<img src="https://i.imgur.com/NJNlTUS.png" height="65%" width="65%" alt="UI to add Role"/>
</p>
<br/>
<p align="center">
<img src="https://i.imgur.com/YKwjpiX.png" height="65%" width="65%" alt="UI to add Role"/>
</p>
</details>    
<hr>
<p align="center"><b>After all of this we should be ready to play with tickets! Aw yeah! :sunglasses:
</b></p>
