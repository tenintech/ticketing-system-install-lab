<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>
<h1>osTicket Help Desk Deployment (Windows Server + IIS + MySQL)</h1>
<h1>Lab Objectives</h1>
Deploy and configure the osTicket ticketing system on a Windows Server virtual machine using IIS, PHP, and MySQL to simulate a real-world IT support environment.  


Deploy a working help desk environment using osTicket on a virtual machine.
Configure a web server and database to support the application.
Create departments, agents, and user accounts within the ticketing system.
Simulate real-world IT support tickets and workflow.
Practice troubleshooting and resolving common IT issues through ticket management.
Document the full deployment and configuration process.


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Internet Information Services (IIS)- Web Server
- MySQL Database 
- Remote Desktop Protocol (RDP)
- PHP - Web Server Language
- Remote Desktop Connection 


<h2>Operating Systems Used </h2>

- Windows 10 V2 x64</b> (22H2)

<h2>List of Prerequisites</h2>

- Create VM to install osTicket
- Install Web Server (IIS) 
- Install Database (MySQL)
- Deploy OS Ticket 
- Item 5

<h2>Installation Steps</h2>

### 1. Create and Connect to a Virtual Machine in Microsoft Azure on which to install ticketing system 

Logged into the Windows Server VM using Remote Desktop Protocol (RDP).
<p>
<img width="935" height="352" alt="4 Connect vm to remote desktop" src="https://github.com/user-attachments/assets/00f19613-8319-4cae-a6ee-8d359eebf112">
</p>
<p>


### 2. Install and Configure Internet Information Services (IIS)
Enabled IIS Web Server and required feature:

Application Development Features → CGI (Common Gateway Inerface) This allows the server to run scripts. 

This allows PHP applications to run on IIS.

<img width="727" height="453" alt="7 Turning on IIS and CGI " src="https://github.com/user-attachments/assets/cc21b4fb-5556-4ba6-9ee2-24c014d11a94" />



### 3. Install Required Dependencies

Installed the required components for osTicket:

- PHP (Hypertext Preprocessor) Manager for IIS
- IIS Rewrite Module
- PHP 7.3
- Visual C++ Redistributable
- MySQL Server

<img width="623" height="423" alt="8  Install PHP " src="https://github.com/user-attachments/assets/8188e11a-27c8-4839-9570-e77745f16e15" />
<img width="692" height="468" alt="9 Installing Rewrite" src="https://github.com/user-attachments/assets/2ca0cf48-6059-4738-8240-083cab722531" />

Created the PHP directory:

C:\PHP

Registered PHP inside IIS.
<img width="875" height="454" alt="13  Register PHP" src="https://github.com/user-attachments/assets/dc1e143c-fa50-47c1-9f5d-918858f97d04" />


### 4. Deploy osTicket to IIS

Extracted the osTicket files and moved them into the web server directory:
<img width="907" height="446" alt="10 Extracting PHP files copying to C drive" src="https://github.com/user-attachments/assets/436ff4a8-aeff-454f-a462-8879245346dd" />

C:\inetpub\wwwroot

Renamed:

upload → osTicket

Restarted IIS.


### 5. Enable Required PHP Extensions
<img width="485" height="437" alt="php extensions enabled" src="https://github.com/user-attachments/assets/df0bd68c-620b-4440-bc9e-f7d676580e8c" />
This resolved the installation warnings. 

p>
<>
</p>
<p>

### 6. Configure the Database

Installed HeidiSQL and created the osTicket database:

Database name:
osTicket

Credentials used:

Username: root
Password: root

</p>
<br />
<img width="731" height="451" alt="20  Connecting to database session " src="https://github.com/user-attachments/assets/462d82ce-97ac-4eb1-b2f3-1e8ef2ed3bd2" />

<p>

</p>
<br />

### 7. Complete osTicket Installation

Finished the setup through the web installer and confirmed the system was operational.

Admin portal:

http://localhost/osTicket/scp/login.php

End user portal:

http://localhost/osTicket/

<p>

<img width="689" height="455" alt="21  osTicket running" src="https://github.com/user-attachments/assets/01a00add-3eb8-4137-9b1b-565b37e27cdb" />


</p>
<p>
<img width="764" height="457" alt="admin dash" src="https://github.com/user-attachments/assets/e52ada2d-c6a4-41fc-bf47-bf349552f000" />

</p>
<br />

<p>
  
### 8. Adding Users and Configuring Service Level Agreements (SLA)




## ⏭️Next Steps

To further build hands-on experience with IT support workflows, I will be expanding this project by working with a more widely used ticketing platform: Zendesk.

In the next phase, I plan to:

Simulate real-world IT support tickets and help desk workflows
Practice troubleshooting and resolving common IT issues through ticket management
Document the lifecycle of support tickets from creation to resolution
Demonstrate how help desk technicians prioritize, escalate, and close incidents

