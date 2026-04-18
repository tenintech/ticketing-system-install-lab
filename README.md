<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>
<h1>osTicket Help Desk Deployment (Windows Server + IIS + MySQL)</h1>
<h1>Lab Objectives</h1>
Deploy and configure the osTicket ticketing system on a Windows Server virtual machine using IIS, PHP, and MySQL, the web server, language and database to support the application in order to simulate a real-world IT support environment. Create departments, agents, and user accounts within the ticketing system.



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
Enabled IIS Web Server and required features so that osTicket can run on the server:

Opened Control Panel -> Programs -> Programs and Features in order to configure IIS

Application Development Features → CGI (Common Gateway Inerface) This allows the server to run scripts. 

This allows PHP applications to run on IIS.

<img width="727" height="453" alt="7 Turning on IIS and CGI " src="https://github.com/user-attachments/assets/cc21b4fb-5556-4ba6-9ee2-24c014d11a94" />



### 3. Install Required Dependencies

Used a folder with installation files to install the required components for osTicket:

- PHP (Hypertext Preprocessor) Manager for IIS
- IIS Rewrite Module
- PHP 7.3
- Visual C++ Redistributable
- MySQL Server

<img width="623" height="423" alt="8  Install PHP " src="https://github.com/user-attachments/assets/8188e11a-27c8-4839-9570-e77745f16e15" />
<img width="692" height="468" alt="9 Installing Rewrite" src="https://github.com/user-attachments/assets/2ca0cf48-6059-4738-8240-083cab722531" />

Created the PHP directory:

C:\PHP

Registered PHP inside IIS. This is a language that will allow osTicket to run.
<img width="875" height="454" alt="13  Register PHP" src="https://github.com/user-attachments/assets/dc1e143c-fa50-47c1-9f5d-918858f97d04" />


Launching the Configuration Wizard for MySql:

<img width="503" height="369" alt="12  mysql installed " src="https://github.com/user-attachments/assets/b2df6209-15d7-4c6f-af05-77adfa57f90f" />


### 4. Deploy osTicket to IIS

Extracted the osTicket php language files and moved them into the web server directory, a file I named PHP on the C Drive:
<img width="907" height="446" alt="10 Extracting PHP files copying to C drive" src="https://github.com/user-attachments/assets/436ff4a8-aeff-454f-a462-8879245346dd" />

C:\inetpub\wwwroot

Renamed:

upload → osTicket

Restarted IIS. Stop and restart server to reset.
<img width="1551" height="944" alt="Screenshot 2026-03-22 005845" src="https://github.com/user-attachments/assets/96af769f-391c-41ea-bb0d-4be3fbc232ec" />



### 5. Enable Required PHP Extensions
Some of needed extensions are disabled. 
<img width="1815" height="958" alt="Screenshot 2026-03-22 011647" src="https://github.com/user-attachments/assets/a9ba9529-9bcb-4117-93f3-1341bd9494f0" />


Enabled some of the extensions listed as prerequisites for installation.
<img width="485" height="437" alt="php extensions enabled" src="https://github.com/user-attachments/assets/df0bd68c-620b-4440-bc9e-f7d676580e8c" />
This resolved the installation warnings. 



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

Opened Advanced Security Settings for os-config file to assign permissions to Everyone in order to make changes in osTicket
<img width="1305" height="955" alt="permissions" src="https://github.com/user-attachments/assets/91be469c-2ed7-41d6-a5e9-a980098603d4" />

<img width="1538" height="955" alt="Screenshot 2026-03-22 012319" src="https://github.com/user-attachments/assets/17709491-05ff-42ac-9e1e-252d350a28e2" />

</p>
<br />

### 7. Complete osTicket Installation

Finished the setup through the web installer and confirmed the system was operational. in System Settings - Named the HelpDesk "Tens Help Desk", added email and selected language.

<img width="721" height="439" alt="18 installing osTicket username" src="https://github.com/user-attachments/assets/bac3b778-9395-491e-a475-243fa7058896" />
<img width="709" height="431" alt="15  osTicket Installer" src="https://github.com/user-attachments/assets/03236a31-19a1-44a7-a619-d0bfc9873042" />
Named an admin user and signed into the portal. 
Admin portal:

http://localhost/osTicket/scp/login.php

End user portal:

http://localhost/osTicket/

<p>

<img width="689" height="455" alt="21  osTicket running" src="https://github.com/user-attachments/assets/01a00add-3eb8-4137-9b1b-565b37e27cdb" />


</p>
<p>
Opened Dashboard of Admin Portal signed in as Teneka.
<img width="764" height="457" alt="admin dash" src="https://github.com/user-attachments/assets/e52ada2d-c6a4-41fc-bf47-bf349552f000" />

</p>
<br />

<p>
  
### 8. Adding Agents and Configuring Service Level Agreements (SLA)

Used admin portal under Departments -> Settings to add a new Department - Sys Admin

<img width="485" height="454" alt="add dept sys admin" src="https://github.com/user-attachments/assets/9f499d23-3c4b-4d9c-9383-e85bdb9f3bf1" />

Created Agent: Michael Snow 
Admin Control --> Agents --> Add New Agent 
<img width="592" height="477" alt="creating agent" src="https://github.com/user-attachments/assets/ad359fc2-2988-4f91-a203-102bd49e8199" />
<p>
   
Set up 3 SLAs:
Manage --> SLA
- Sev-A (Grace Period: 1 hour, Schedule: 24/7)
- Sev-B (Grace Period: 4 hours, Schedule: 24/7)
- Sev-C (Grace Period: 8 hours, Business Hours)


Admin Panel -> Manage -> SLA
<p>

<img width="542" height="454" alt="create sla" src="https://github.com/user-attachments/assets/c37440b4-5372-4994-942c-5a5173b6ac0a" />

## What I Learned 
Installing the ticketing system taught me essential IT service management (ITSM) skills, like workflow automation, ticket categorization, and SLA management. I learned to configure portals and permissions, and learned some functions an administrator might perform to set up a ticketing system for a new organizaton and onboard new agents. 

## ⏭️Next Steps

In the next lab, I will be expanding this project by working with a more widely used ticketing platform: Zendesk.

I plan to:

- Simulate real-world IT support tickets and help desk workflows
- Practice troubleshooting and resolving common IT issues through ticket management


