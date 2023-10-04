# osticket-prereqs
<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This walkthrough descripts how to install osTicket system through azure virtual machine.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)
- Google doc download (below)
- https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

-Azure virtual machine(VM)

-Enable IIS on VM

-Open googledoc download thru VM

-Install Each download 

<h2>Installation Steps</h2>


<p>
<img src="https://i.imgur.com/FHJAcRp.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>
On azure get IP address by connecting VM.
<br />

<p>
<img src="https://i.imgur.com/HFOoW2k.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>
Open Remote desktop conection app on computer to connect to VM. remember what the username for vm is and log in.
</p>
<br />

<p>
<img src="https://i.imgur.com/1FolywO.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>
Once in VM search control panel click programs then programs and features, as pictured above click Windows features.
</p>
<br />

<p>
<img src="https://i.imgur.com/8XizlPp.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/HuH1IWN.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
Under Windows features Install and Enable IIS Management Console and CGI and Common HTTP Features thru World Wide Web Services -> Application Development Features -> click CGI. also under Internet Information Services -> Web Management Tools, check IIS Management Console click ok and should install all features.
</p>
<br />

<p>
<img src="https://i.imgur.com/qTLSbO6.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>
with google link download everything on list to install on VM. 
https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6
</p>
<br />

<p>
<img src="https://i.imgur.com/G7CtvPf.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/lmMsbO9.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/qpyDq25.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
Once downloaded open file, then open and install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi), Rewrite Module (rewrite_amd64_en-US.msi).
</p>
<br />

<p>
<img src="https://i.imgur.com/EwPxSQE.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>
you will need a new folder, Create C:\PHP
</p>
<br />

<p>
<img src="https://i.imgur.com/CEaAvDA.png" height="45%" width="45%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/YUOGncq.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
Then back in installation files, open PHP 7.3.8 zipped folder and copy all files to new created PHP folder.
</p>
<br />

<p>
<img src="https://i.imgur.com/wls0Hce.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>
Next step download and install VC_redist.x86.exe.
</p>
<br />

<p>
<img src="https://i.imgur.com/daKK4lh.png" height="35%" width="35%" alt="Disk Sanitization Steps"/>
</p>
After VC, download and install MySQL 5.5.62 (mysql-5.5.62-win32.msi)
</p>
<br />
<img src="https://i.imgur.com/q0T2oEz.png" height="35%" width="35%" alt="Disk Sanitization Steps"/>
<p>
for setup install with Typical setup
</p>


<p>
<img src="https://i.imgur.com/qTqAtaT.png" height="35%" width="35%" alt="Disk Sanitization Steps"/>
</p>
Then in Configuration Wizard (after install), install with Standard Configuration
</p>
<br />

<p>
<img src="https://i.imgur.com/ep90Dum.png" height="35%" width="35%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/8BwhAT2.png" height="35%" width="35%" alt="Disk Sanitization Steps"/>
</p>
Install as windows service and setup with personal password for SQL.
</p>
<br />

<p>
<img src="https://i.imgur.com/qTqAtaT.png" height="35%" width="35%" alt="Disk Sanitization Steps"/>
</p>
Then in Configuration Wizard (after install), install with Standard Configuration
</p>
<br />

<p>
<img src="https://i.imgur.com/Gq5vrtK.png" height="35%" width="35%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/t4ujaI7.png" height="35%" width="35%" alt="Disk Sanitization Steps"/>
</p>
Open IIS as an Admin Then restart server.
</p>
<br />

<p>
<img src="https://i.imgur.com/BJl9x80.png" height="45%" width="45%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/hAFHUrJ.png" height="45%" width="45%" alt="Disk Sanitization Steps"/>
</p>
Then in IIS open PHP manager and Register PHP by seraching for file like dipicted in picture above. next you will scoll down in PHP manager and click enable extensions
</p>
<br />

<p>
<img src="https://i.imgur.com/iaaNrIw.png" height="45%" width="45%" alt="Disk Sanitization Steps"/>
</p>
For PHP extensions scroll down to right click and enable php_imap.dll, php_intl.dll, php_opcache.dll, should look like the picture above as highlighted.
</p>
<br />

<p>
<img src="https://i.imgur.com/jyXeyJP.png" height="65%" width="65%" alt="Disk Sanitization Steps"/>
</p>
Back in installations files open folder osTicket v1.15.8, then Extract and copy “upload” folder to c:\inetpub\wwwroot
</p>
<br />

<p>
<img src="https://i.imgur.com/SPdNS6g.png" height="65%" width="65%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/5ylICRO.png" height="65%" width="65%" alt="Disk Sanitization Steps"/>
</p>
then open c:\inetpub\wwwroot and rename upload file to osTicket.
</p>
<br />

<p>
<img src="https://i.imgur.com/UUFAd6X.png" height="65%" width="65%" alt="Disk Sanitization Steps"/>
</p>
Go to IIS-> sites -> Default -> osTicket, on the right, click “Browse *:80”
</p>
<br />

<p>
<img src="https://i.imgur.com/bpPEmN2.png" height="35%" width="65%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/fdKN1yt.png" height="35%" width="65%" alt="Disk Sanitization Steps"/>
</p>
Then in windows open C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php and rename C:\inetpub\wwwroot\osTicket\include\ost-config.php (just delete word sample from file).
</p>
<br />

<p>
<img src="https://i.imgur.com/uUuFJpZ.png" height="25%" width="25%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/4zKCnEa.png" height="45%" width="45%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/v4iGecH.png" height="35%" width="35%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/4QGBio1.png" height="35%" width="35%" alt="Disk Sanitization Steps"/>
</p>
Assign Permissions to ost-config.php by right clicking to properties into security 
Disable inheritance -> Remove All
New Permissions -> Everyone -> All

</p>
<br />

<p>
<img src="https://i.imgur.com/s8WDRn0.png" height="65%" width="65%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/adSlr0Y.png" height="35%" width="65%" alt="Disk Sanitization Steps"/>
</p>
Continue Setting up osTicket in the browser (click Continue)
Name Helpdesk
Default email (receives email from customers)
remember all info to login in later.
</p>
<br />

<p>
<img src="https://i.imgur.com/PQDzcQJ.png" height="35%" width="65%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/GgvrAxW.png" height="35%" width="65%" alt="Disk Sanitization Steps"/>
</p>
From the Installation Files, download and install HeidiSQL.
Open Heidi SQL
Create a new session, root/Password1
Connect to the session
Create a database called “osTicket”

</p>
<br />

<p>
<img src="https://i.imgur.com/34fj4tO.png" height="65%" width="65%" alt="Disk Sanitization Steps"/>
</p>
Continue Setting up osticket in the browser

-MySQL Database: osTicket

-MySQL Username: root

-MySQL Password: Password1

-Click “Install Now!”

</p>
<br />

<p>
<img src="https://i.imgur.com/LRPyahD.png" height="65%" width="65%" alt="Disk Sanitization Steps"/>
</p>
And Viola should get a page like this in browser.
</p>
<br />
