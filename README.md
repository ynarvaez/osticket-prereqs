<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Install and enable IIS with CGI and common HTTP features
- Download and install PHP Manager for ISS
- Download and install The Rewrite Model
- Create the directory C:\PHP
- Download PHP and unzip the contents into C:\PHP
- Download and install VC_redist.x86.exe.
- Download and install MYSQL
- Open IIS as and Admin
- Register PHP from within IIS
- Reload IIS
  
<h2>Installation Steps</h2>

Install osTicket v1.15.8

Download osTicket from the Installation Files Folder

Extract and copy “upload” folder to c:\inetpub\wwwroot

Within c:\inetpub\wwwroot, Rename “upload” to “osTicket”

Reload IIS (Open IIS, Stop and Start the server)

Go to sites -> Default -> osTicket
On the right, click “Browse *:80”

</p>
<br />




<p>


</p>
<p>
Note that some extensions are not enabled

Go back to IIS, sites -> Default -> osTicket

Double-click PHP Manager

Click “Enable or disable an extension”

Enable: php_imap.dll

Enable: php_intl.dll

Enable: php_opcache.dll

Refresh the osTicket site in your browse, observe the changes

</p>
<br />

<p>
<img src="https://i.imgur.com/Js5zmnH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Rename: ost-config.php

From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php

To: C:\inetpub\wwwroot\osTicket\include\ost-config.php
<img src="https://i.imgur.com/CFpfGiz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

Assign Permissions: ost-config.php

Disable inheritance -> Remove All

New Permissions -> Everyone -> All
<img src="https://i.imgur.com/siiM1wB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

</p>
<br />
Continue Setting up osTicket in the browser (click Continue)

Name Helpdesk

Default email (receives email from customers)


From the Installation Files, download and install HeidiSQL.

Open Heidi SQL

Create a new session, root/Password1

Connect to the session

Create a database called “osTicket”

Continue Setting up osticket in the browser

MySQL Database: osTicket

MySQL Username: root

MySQL Password: Password1

Click “Install Now!”

