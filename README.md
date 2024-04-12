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

- Windows 10</b> (22H2)

<h2>List of Prerequisites</h2>

- IIS and Management Console
- PHP and Rewrite Module
- MySQL
- HeidiSQL
- osTicket

<h2>Installation Steps</h2>

<p>
<img width="570" alt="image" src="https://github.com/jaydcollins/ticket-lifecycle/assets/164976272/505b7e93-d47b-467c-a4f3-50ae245e4444">
</p>

- Create a virtual machine that hosts Windows 10.
- Install IIS by right-clicking on the start button, click on "run" and type in "Control Panel", hit OK.
- Navigate to Programs and Features. Select "Turn Windows features on or off".
- Enable "Internet Information Services"
- Internet Information Services -> Web Management Tools enable IIS Management Console
- Internet Information Services -> World Wide Web Services -> Common Features enable all Common HTTP Features 
- Internet Information Services -> World Wide Web Services -> Application Development Features enable CGI

<br />

<p>
<img width="680" alt="image" src="https://github.com/jaydcollins/ticket-lifecycle/assets/164976272/746a9d24-fe9d-439b-a8ba-1906f43399ab">
</p>

- Install PHP Manager for IIS. 
- Install Rewrite Module.
- Create a folder in C:\ called "PHP".
- Download PHP 7.3.8 or higher and unzip contents to "PHP" folder you created.
- Install Microsoft Visual C+ redist.x86.exe.
- Install MySQL (typical setup).
- Launch MYSQL configuration wizard, select Standard Configuration and create a root password- you will need to remember it later. Hit Execute and Finish.

<br />

<p>
<img width="657" alt="image" src="https://github.com/jaydcollins/ticket-lifecycle/assets/164976272/1c01aebd-7f59-47f1-840a-742145b6101f">
</p>

- Open IIS as administrator.
- Navigate to PHP Manager. Select Register new PHP version. Click the ... and navigate to C:\PHP\php-cgi. Hit Open and OK.
- Restart the server. 
- Download osTicket. 
- Extract and copy "upload" folder to C:\inetpub\wwwroot
- Rename the "upload folder to "osTicket". 
- Reload IIS (restart the server). 
- Go to: Sites > Default Web Site > osTicket. On the far right of the window, click on "Browse*:80". 
- Go to C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php and rename "ost-sampleconfig.php" to "ost-config.php". 
- Next, you will need to enable PHP extensions before continuing with osTicket. 
- Go back to IIS and go to Sites > Default Web Site > osTicket. Double click on PHP manager and then click "Enable or disable an extension". Enable "php_imap.dll", "php_intl.dll" and "php_opcache.dll". 
- Right click on ost-config.php and assign file permissions to everyone (Disable inheritance > Remove All, New Permissions > Everyone > All). 
- Refresh the browser, showing osTicket, and observe the changes to osTicket's PHP extensions.
  
<br />


<p>
<img width="803" alt="image" src="https://github.com/jaydcollins/ticket-lifecycle/assets/164976272/d4db0bb0-4737-44e0-a35b-de23a5cc38b0">
</p>

- Start filling out the Helpdesk and admin user sections in osTicket. 
- Before you fill in Database Settings, we will need a database client.
- Install HeidiSQL.
- Open HeidiSQL and create a new database using the name and password you created for MySQL.
- Connect to session and create a database called "osTicket". Now that you've created a database you can now finish filling out the form. Use your MySQL name and password on the form.
- Click Install.
- Browse to your help desk login page: http://localhost/osTicket/scp/login.php. Now for a little bit of cleanup.
- Use file explorer to navigate to and delete: C:\inetpub\wwwroot\osTicket\setup.
- Set permissions to “Read, Read and Execute" at : C:\inetpub\wwwroot\osTicket\include\ost-config.php.


<br />

<h2 align="center"> Great Job! OsTicket is installed and ready for us to configure. </h2>
