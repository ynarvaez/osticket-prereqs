<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Computer)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

<b>Open this:</b> <a href="https://drive.google.com/drive/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6">Installation Files </a>
<br>
<i>These are the installation files that will be used to install osTicket and some of the dependencies.</i> 
<br>
<br>
<b>1. Install / Enable IIS in Windows WITH
CGI and Common HTTP Features </b>
- World Wide Web Services -> Application Development Features ->
<br> [X] CGI
<br> [X] Common HTTP Features<br><b>AND IIS Management Console</b>
  - Internet Information Services -> Web Management Tools -> IIS Management Console
<br>[X] IIS Management Console

<b>2. Download/Install PHP Manager for IIS</b>

<b>3. Download/Install Rewrite Module</b>

<b>4. Create the directory C:\PHP</b>

<b>5. Download/Install PHP 7.3.8 and unzip contents into C:\PHP</b>

<b>6. Download/Install VC_redist.x86.exe</b>

<b>7. Download/Install MySql 5.5.62</b>
  - Typical Setup ->
  - Launch Configuration Wizard (after install) ->
  - Standard Configuration ->
  - Take note of username: root
  - Example Password: Password1

<b>8. Open IIS as an Admin</b>

<b>9. Register PHP from within IIS</b>

<b>10. Reload IIS (Open IIS, Stop and Start the server)</b>
   - Download/Install osTicket
   - Extract and copy “upload” folder to c:\inetpub\wwwroot
   - Within c:\inetpub\wwwroot, Rename “upload” to “osTicket”

<b>11. Reload IIS (Open IIS, Stop and Start the server)</b>

<b>12. Go to sites -> Default -> osTicket</b>
   - Click "Browse *.80" on the right

<b>13. Enable extensions that are off</b>
   - Go back to IIS, sites -> Default -> osTicket
   - Double-click PHP Manager
   - Click “Enable or disable an extension”
	- Enable: php_imap.dll
	- Enable: php_intl.dll
	- Enable: php_opcache.dll

<b>14. Refresh the osTicket site to view updates</b>

<b>15. Rename: ostsample-config.php to ost-config.php</b>
   - From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
   - To: C:\inetpub\wwwroot\osTicket\include\ost-config.php


<b>16. Assign Permissions: ost-config.php</b>

   - Right click ost-config.php
   - Click security -> Advanced settings
   - Disable inheritance -> Remove All
   - Click Select a principal
   - New Permissions -> Everyone -> All
   - Apply -> Ok


<b>17. Download and install HeidiSQL</b>
<br>
- Open Heidi SQL
- Create a new session, root/Password1
- Connect to the session
- Right click and create a database called “osTicket”

<b>18. Continue Setting up osTicket in the browser (click Continue)</b>
- Example Name: Helpdesk
- Default email (receives email from customers)


<b>19. Continue Setting up osticket in the browser(Click Continue) </b>
   - MySQL Database: osTicket
   - MySQL Username: root
   - MySQL Ex. Password: Password1
   - Click “Install Now!”


<b>20. Congratulations! osTicket should be installed without any errors.</b>
  - Browse to your help desk login page: http://localhost/osTicket/scp/login.php </a>
  - End Users osTicket URL: http://localhost/osTicket/


<b>21. Clean up</b>
   - Delete: C:\inetpub\wwwroot\osTicket\setup
   - Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php


<h2>Installation Steps</h2>

<i>Below are a few visual steps to help assist with installation.</i>
<br>
<i>Numbers represent the corresponding steps from above.</i>


<b>1. Open control panel, click programs then "Turn Windows features on or off"</b>
<br>
<br>
<b> Install / Enable IIS in Windows WITH
CGI and Common HTTP Features </b>
- World Wide Web Services -> Application Development Features ->
<br> [X] CGI
<br> [X] Common HTTP Features<br>


  <img width="376" alt="image" src="https://github.com/nkgarrett/osticket-prereqs/assets/156832893/6eac08b3-39eb-488e-a86d-4e9f27218738">


	 
  <b>AND IIS Management Console</b>
  - Internet Information Services -> Web Management Tools -> IIS Management Console
<br>[X] IIS Management Console
<img width="376" alt="image" src="https://github.com/nkgarrett/osticket-prereqs/assets/156832893/12e8a8cc-cb9e-43b0-8156-af50bee10b8e">
<br>
<br>
<p>
4. <b>Create the directory C:\PHP</b>
</p>	
 	<img width="465" alt="image" src="https://github.com/nkgarrett/osticket-prereqs/assets/156832893/f21d6cf5-7e4c-414f-9cf5-565ccbf3a7ec">
<br>
<br>
<p>
5. <b>Download/Install PHP 7.3.8 and Unzip contents into C:\PHP</b>
</p>	
	<img width="569" alt="image" src="https://github.com/nkgarrett/osticket-prereqs/assets/156832893/7af6fae8-cb43-4d5a-82e7-dfb5179794a5">
 <br>
 <br>
<p>
8. <b>Open IIS as an Admin. Click start menu, search IIS and right click it to "run as administrator"</b>
</p>
	 <img width="320" alt="image" src="https://github.com/nkgarrett/osticket-prereqs/assets/156832893/fee3bb64-4a61-4466-a648-93fdc1f4da77">
  <br>
  <br>
<p>
9. <b>Register PHP from within IIS</b>
   - Go to PHP Manager
   - Click Register new PHP version
</p>	
   <img width="508" alt="image" src="https://github.com/nkgarrett/osticket-prereqs/assets/156832893/19e9868f-7e6c-46a5-b318-71f0d190c444">
<br>
<br>
<p>
13.<b> Enable extensions that are off</b>
</p>	
    <p>Before: </p>
    <img width="508" alt="image" src="https://github.com/nkgarrett/osticket-prereqs/assets/156832893/f8846350-35bf-446a-b3a1-9adb7791e2d4"> 
<br>
<br>
<p>   
14.<b> Refresh the osTicket site to view updates</b>
</p>
    <p>After: </p>
    <img width="508" alt="image" src="https://github.com/nkgarrett/osticket-prereqs/assets/156832893/56a6610d-cd34-4cda-a02f-491682a02b4b">
 <br>
 <br>
 <p>
 19. <b>Congratulations! osTicket should be installed without any errors.</b>
<br>
<br>
    <img width="577" alt="image" src="https://github.com/nkgarrett/osticket-prereqs/assets/156832893/e48f4c1d-d123-4d8f-a25b-8780333e181b">
 </p>

</p>
<br />

<p>

</p>
<p>

</p>
<br />
