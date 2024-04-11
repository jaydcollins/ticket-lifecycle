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
<img src="https://github.com/kphillip1/osticket-prereqs/assets/165929885/ef3ab4ed-3ec5-40d8-9e63-fda93969d77d" height="80%" width="80%"/>
</p>

- Create a virtual machine that uses Windows 10.
- Install IIS by right-clicking on the start button, click on "run" and type in "control panel".
- Select program and features. Select "windows features". Install and enable IIS management console in web management tools.
- In addition, enable CGI and all of Common HTTP Features boxes (located in: world wide web services > application development features.) 
- Install PHP manager. 
- Install rewrite module.

<br />

<p>
<img src="https://github.com/kphillip1/osticket-prereqs/assets/165929885/9a9e407a-1149-4938-8e10-3127de7ba463" height="80%" width="80%"/>
</p>

- Create a folder in C:\ called "PHP".
- Install PHP and unzip contents to PHP folder you created.
- Install VC redist.x86.exe. Install MySqL (typical setup).
- Launch configuration wizard, select standard and create a name plus password. FYI- You will need to remember them.

<br />

<p>
<img src="https://github.com/kphillip1/osticket-prereqs/assets/165929885/1e2a2dc5-1f91-430d-a6a2-60d680e44cad" height="80%" width="80%" />
</p>

- Open IIS as administrator. 
- Register PHP inside of IIS. 
- Stop and start server. 
- Install osTicket. 
- Extract "uploads" folder to C:\inetpub\wwwroot. 
- Rename the folder "osTicket". 
- Reload IIS (Stop and start server). 
- Go to: sites > default > osTicket; on the far right of the window, click on "Browse*:80". 
- Go to C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php and rename "ost-sampleconfig.php" to "ost-config.php". 
- Next, you will need to enable PHP extensions before continuing with osTicket. 
- Go back to IIS and go to "sites > default > osTicket. Double click on PHP manager and then click on "Enable or disable an extension". 
- Assign file permissions to everyone (Disable inheritance > Remove All, New Permissions > Everyone > All). Enable "php_imap.dll", "php_intl.dll" and "php_opcache.dll". 
- If you refresh the browser, osTicket's PHP extension changes will be shown.
  
<br />

<p>
<img src="https://github.com/kphillip1/osticket-prereqs/assets/165929885/2f1e0dee-8d77-4180-9e50-bf8f79663b18" height="80%" width="80%" />
</p>

- Start filling out the form in os Ticket. 
- Before you complete the form, you'll need a database client.
- Install HeidiSQL.
- Open HeidiSQL and create a new database using the name and password you created for MySQL.
- Connect to session and create a database called "osTicket". Now that you've created a database you can now finish filling out the form. Use your MySQL name and password on the form.
- Click install now.
- Browse to your help desk login page: http://localhost/osTicket/scp/login.php. There's a little bit of cleanup necessary before you proceed.
- Delete: C:\inetpub\wwwroot\osTicket\setup.
- Set permissions to “Read, Read and execute" at : C:\inetpub\wwwroot\osTicket\include\ost-config.php.


<br />

<h2 align="center"> Nice work! OsTicket is installed and ready to be configured. </h2>
