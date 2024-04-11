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

- Internet Information Services(IIS)
- MySQL 5.5
- Simple versions of x86 PHP up to v7.3
- osTicket v1.15.8


<h2>Installation Steps</h2>

<p>
<img width="264" alt="image" src="https://github.com/jaydcollins/ticket-lifecycle/assets/164976272/b8778c07-5996-4b90-8b3d-6b6c062a424a">



</p>
<p>
Install or enable IIS. Open the control panel. IIS will will enable a web server on your computer to run osTicket. Type "Control Panel" from your search bar in the task bar at the bottom of your desktop. 
</p>
<br />
<p>
<img width="571" alt="image" src="https://github.com/jaydcollins/ticket-lifecycle/assets/164976272/f5b09cf1-cfe5-44a6-93c3-69c527fa82e7">
</p>
<p> 
Once you have the control panel open, navigate to the "Programs and Features" section and click on the "Turn Windows features on or off" link.
</p>
<br />
<p>
<img width="575" alt="image" src="https://github.com/jaydcollins/ticket-lifecycle/assets/164976272/067db0c6-3fae-4c68-bbc5-b17a041dc4fe">
</p>
<p>
</p>
<p>
Scroll down and find the "Internet Information Services" option. Check the box next to this option. Click the + sign on the World Wide Web Services -> Application Development Features and check the boxes for CGI and Common HTTP Features. Click the + sign on Internet Information Serves -> Web Management Tools -> IIS Management Console and check the box for IIS Management Console. 
</p>
<br />
<p>
<img src="https://i.imgur.com/7wr3cJ5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Click the "OK" button to install IIS. This may take a few minutes, depending on your system.
Once IIS has been installed, search the internet for Microsoft Web Platform Installer and download this extension.  You will need it to install the remaining software needed to install osTicket. 
</p>
<br />
<img src="https://i.imgur.com/JYFycyo.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<br />
<p>
<img src="https://i.imgur.com/5FxYjjm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Search and install : "Web Platform Installer" From the Internet. Open "Web Platform Installer". In the search box of Web Platflorm Installer, add "MySQL 5.5". Search and add all simple versions of (x86) PHP up until 7.3. 
</p>
<br />
<p>
<img src="https://i.imgur.com/zfYBcGT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Create a username and password.(Make sure to remeber these credentials.)
</p>
<br />
<p>
<img src="https://i.imgur.com/WcXKg0A.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Web installer will attempt to finish installing all of the prerequistes that are checked some of the downloads will fail, manually download C++ Redistribuable & PHP Manager(You will have to go on the internet to find these files). Continue to finish with installation. Find and install "PHP Manager" version 7.3.8 & version 1.5.0.
</p>
<br />
<p>
</p>
<p>
Install Microsoft Visual C++ 
</p>
<br />
<p>
</p>
<p>
Install PHP Manager
</p>
<br />
<p>
</p>
<p>
Installation errors should be fixed at this point.  Download and install the osTicket software.  You will need to 'Extract' the zip file. 
</p>
<br />
<p>
<img src="https://i.imgur.com/nrGl3xr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once osTicket has been installed, open the download folder and copy it into your'wwwroot'folder that was created from IIS and rename the folder from 'upload' to 'osTicket'. Filepath--> ThisPC/Windows(C:)/-->inetpub/wwwroot
</p>
<br />
<p>
<img src="https://i.imgur.com/3Pd9cBn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
</p>
<br />
<p>
<img src="https://i.imgur.com/FCnEwfr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Go to Search Taskbar and Type 'IIS' in the searchbar and open the program. You will need to restart the web server by selecting the 'browse 80 folder' in the connections folder. Click 'Sites' -> 'osTicket' -> 'browse80' -> 'Stop' -> 'Restart'
</p>
<br />
<br />
<p>
<img src="https://i.imgur.com/k9NGbg0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Program should have installed properly.
</p>
<br />
<br />
<p>
<img src="https://i.imgur.com/csbuByY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Enable the following extenions, 'php_imap.dll', 'php_intl.dll', and 'php_opcache'. Reset osTicket site and observe changes
</p>
<br />
<br />
<p>
<img src="https://i.imgur.com/TXQyeeN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Go to 'ThisPC' > 'Windows(C:)' > 'inetpub' > 'wwwroot' > 'osTicket' > 'include'.  Find and Rename 'ost-sampleconfig.php' and rename to 'ost-config.php'
</p>
<br />
<br />
<p>
<img src="https://i.imgur.com/mylaQhw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Enable automatic permissions for everyone in this file by right-clicking on the file and select ->Properties >Advanced >Disable inheritance >Type everyone in the next dialog box-->selct Full Control.Apply button-->Select the Ok button 
</p>
<br />
<br />
<p>
</p>
<p>
Download and install HeidiSQL for osTicket to have a client database that connects to MySQL that was installed previously. 
</p>
<br />
<br />
<p>
<img src="https://i.imgur.com/AiBuuKV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
To create a database, you will need the username and password that was used to install MySQL.  Create a new database by right-clicking on SSS-->New-->Database-->> name your database osTicket and click Ok.
</p>
<br />
<br />
<p>
<img src="https://i.imgur.com/thE2GQW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Go to your osTicket installer in your browser tab and fill out the following information in the fields.  --> System Settings-->Admin User-->Database Settings--> Click on "Install Now" 
</p>
<br />
<br />
<p>
<img src="https://i.imgur.com/O2maQA7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
This screen will show a successful installation of osTicket
</p>
<br />
<br />
<p>
<img src="https://i.imgur.com/RW2GZ7K.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Go to your C:-->inetpub-->wwwroot-->osTicket and delete the 'setup' file. You may have to delete contents inside first to delete file.
</p>
<br />
<br />
<p>
<img src="https://i.imgur.com/tbrMTeT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Go to C:-->Inetpub-->wwwroot-->osTicket-->inlclude and right click on ost-config.php and select securities tab-->advanced-->click edit to change permissions for everyone to only have read & execute by deselecting the radio buttons.  Click on apply-->Ok
</p>
<br />
<br />
<p>
<img src="https://i.imgur.com/mznjwS9.png" width="80%" alt="Disk Sanitization Steps"/>
<p>
Once osTicket is installed, you can access it from a web browser by typing the URL of your web server into the address bar (e.g. "http://localhost"). This will open the osTicket login page, where you can log in and start using the application.
