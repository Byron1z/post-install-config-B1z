<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10 Pro</b> (22H2)

<h2>Post-Install Configuration Objectives</h2>

- Configure Roles
- Configure Departments
- Configure Teams
- Allow Anyone to Create Tickets
- Configure Agents
- Configure End Users
- Configure SLA
- Configure Help Topics
<br />
<h2>Configuration Steps</h2>
<p>
  Here we are going to Explore and set up additional configurations for osTicket Portal before we actually start creating & solving mock tickets.

  Here are the Different Panels to Acknowledge, 1st would be the Admin Panel, which is where the Sys Admin would work and configure settings.
</p>
<p>
<img src="https://i.imgur.com/7m7gC6O.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
And here would be the Agent Panel where normal help desk workers will be working.
</p>
<p>
  <img src="https://i.imgur.com/v6eR3qF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<h3>Configure Roles</h3>
<p>
  Configure Roles (for grouping permissions), 
  Here we are going to group permissions and giving permissions to certain people.

  Admin Panel -> Agents -> Roles, create Supreme Admin and give all permissions.
  
● Supreme Admin
</p>
<p>
<img src="https://i.imgur.com/x04nzJM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/I4BRe8r.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/VghqyYc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/POiKGpB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<h3>Configure Departments</h3>
<p>
  Configure Departments (Ticket Visibility, Help Desk vs Sys Admins, vs Networking) 

  Admin Panel -> Agents -> Departments, create New Department

  ● SysAdmins

(This is for Ticket Visibility such as for Help Desk, Sys Admin, or for Networking. An example would be if a Ticket is assigned to the Network Department, we can configure it so only they can see their own tickets, or implement settings to give the Sys Admin ability to see all tickets)

(leave it at “Top Level Department”)
</p>
<p>
<img src="https://i.imgur.com/To8HAcG.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/ouhR4tX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<h3>Configure Teams</h3>
<p>
Configure Teams
  
Admin Panel -> Agents -> Teams (Pull a group of Agents from different Departments) 

  ● Online Banking
</p>
<p>
  <img src="https://i.imgur.com/G9EeeBT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<h3>Allow anyone to Create Tickets</h3>
<p>
  Allow anyone to Create Tickets 

  Admin Panel -> Settings -> User Settings (UNCHECK: unregistered users can create 
tickets) 

  ● Registration Required: Require registration and login to create tickets (UNCHECK)
</p>
<p>
  <img src="https://i.imgur.com/pye2jve.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<h3>Configure Agents</h3>
<p>
  Configure Agents (Workers) 

  Admin Panel -> Agents -> Add New Agent

● Byron (Dept: SysAdmins, Supreme Admin) 

● Hilda (Dept: Support)

Create Byron who is a Supreme Admin
</p>
<p>
  <img src="https://i.imgur.com/l4DvtHn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
   <img src="https://i.imgur.com/9cqVxov.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  Next, Create Agent Hilda who is in Support.
</p>
<p>
 <img src="https://i.imgur.com/CMfM0bD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 <img src="https://i.imgur.com/3w3bXk8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  Here are the Agents
</p>
<p>
  <img src="https://i.imgur.com/gbKXZkb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<h3>Configure End-Users </h3>
<p>
  Configure End-Users (Customers) 

  Agent Panel -> Users -> Add New User 

● Marianne 
</p>
<p>
  <img src="https://i.imgur.com/Y7uCuMK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/22zxRMx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<h3>Configure SLA </h3>
<p>
  Configure SLA 

  Admin Panel -> Manage -> SLA, Add New SLA Plan

● Sev-A (Grace Period: 1 hour, Schedule: 24/7) 

● Sev-B (Grace Period: 4 hours, Schedule: 24/7) 

● Sev-C (Grace Period: 8 hours, Business Hours)

(SLA stands for Service Level Agreement which is how much time to do some specific tasks whether it is Responding or Completing a Ticket)

SLAs Plans provide a length of time in which the Help Desk is expected to take in order to troubleshoot or solve a specific ticket.
Each SLA has a schedule and within that schedule there is a grace period. 

In this example SEV-A has a 24/7 and a one hour grace period, which is too soon to solve, but we can always change it.
</p>
<p>
  <img src="https://i.imgur.com/GYYSSEG.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/3mYicAc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<h3>Configure Help Topics</h3>
<p>
  Lastly, we Configure Help Topics (For when Users create a Ticket) 

  Admin Panel -> Manage -> Help Topics, Add New Help Topics

● Business Critical Outage -> Report a problem

● Personal Computer Issues -> Report a problem

● Equipment Request -> General Inquiry 

● Password Reset ->General Inquiry 

● Other

Help topics are categories to help users categorize their tickets. 

In the 1st example below we have made a help topic for "Business Critical Outage" this can be if customers cannot access mobile banking.
</p>
<p>
  <img src="https://i.imgur.com/JDaXQYz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/XdKpGOW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
