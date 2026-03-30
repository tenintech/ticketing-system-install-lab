<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>
<h1>osTicket Help Desk Deployment (Windows Server + IIS + MySQL)</h1>
<h1>Lab Objectives</h1>
  
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
1. Create and Connect to a Virtual Machine in Microsoft Azure on which to install ticketing system 

Logged into the Windows Server VM using Remote Desktop Protocol (RDP).
<p>
<img width="935" height="352" alt="4 Connect vm to remote desktop" src="https://github.com/user-attachments/assets/00f19613-8319-4cae-a6ee-8d359eebf112">
</p>
<p>


2. Install and Configure Internet Information Services (IIS)
Enabled IIS Web Server and required feature:

Application Development Features → CGI (Common Gateway Inerface) This allows the server to run scripts. 

This allows PHP applications to run on IIS.


3. Common Gateway Interface (CGI)
Configure IIS 
Register Hypertext Preprocessor (PHP) making web server aware that PHP is on the computer 
Extract osTicket folder and copy into the root folder of the web server 
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
 Within the virtual machine, I downloaded the required osTicket Installation Files and saved them locally to the desktop. I then extracted the contents into a structured directory named osTicket-Installation-Files, ensuring all required installation dependencies and components were properly organized before application deployment.Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
Ticketing System Installation Lab
Objective

Install and configure a help desk ticketing system.

Technologies / Environments Used
osTicket
Apache / IIS
MySQL / MariaDB
Linux or Windows server
Lab Steps
Step 1 — Create Server

Deploy a virtual machine for the ticket system.

Step 2 — Install Required Software

Install:

Web server
PHP
MySQL database
Step 3 — Download osTicket

Download osTicket and place it in web directory.

Example:

/var/www/html/osticket
Step 4 — Create Database

Create database:

osticket_db
Step 5 — Run Installer

Open browser:

http://server-ip/osticket

Complete setup.

Outcome

Working help desk ticket system.

# ticketing-system-install-lab
