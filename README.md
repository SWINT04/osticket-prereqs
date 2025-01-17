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

- Azure Virtual Machine
- oSticket Installation files
- Heidi SQL


<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/gbTQzwK.png height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Hello and welcome, I will show you how to install Osticket. First we will be creating a Virtual machine using the Microsoft Azure portal. We are using a VM in order to create space and manage operating systems. Next we will Create a resource group and name it "Rg-osTicket". Then we will create a VM with 2 or 4 CPUs. In the example above I will be using 4 CPUs.
</p>
<br />

<p>
<img src="https://i.imgur.com/XxsU46B.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, we will connect to the virtual machine by using remote desktop connection or if you are a mac user like me we will be using the downloadable app called microsoft remote desktop. Next we will copy and paste the public ipv4 address to connect to our virtual machine.
</p>
<br />

<p>
<img src="https://i.imgur.com/2tx7zmC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next we are going to Install/Enable Internet Information Services (IIS) along with CGI.
</p>
<br />

<p>
<img src=https://i.imgur.com/qiO1C74.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next we need to download "Php manager". Here is a link for all the files you need to download to set up osTicket: https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6. 
</p>
<br /v

<p>
<img src=https://i.imgur.com/D8WxClb.png height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next we are going Install "rewrite module" from the installation files.
</p>
<br /v

<p>
<img src=https://i.imgur.com/Vc5WJ5H.png height="80%" width="80%" alt="Disk Sanitization Steps"/>
</P>
<P>
Create the directory C:\PHP
</P>
<br /v

<p>
<img src= https://i.imgur.com/tGZU7xq.png height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
From the Installation Files, download PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) then extract all files into C:\PHP
</p>
<br /v

<p>
<img src= https://i.imgur.com/SLU8noU.png height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
From the Installation Files, download and install VC_redist.x86.exe.
</p>
<br /v
<p>
<img src= https://i.imgur.com/4tjAqjk.png height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In the installation files, download and install MySQL 5.5.62 (mysql-5.5.62-win32.msi). First hit typical-> check box that reads "launch the MySQL instance configuration wizard"-> Hit finish, then hit next..click the box for standard config-> then click install as windows server->Type your preference for password-> continue into modify security settings; tap execute and hit finish. 
</p>
<br /v
<p>
<img src= https://i.imgur.com/DJzZVZj.png height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Right click IIS in the start menu, then click run as admin-> double click php manager-> register new php version-> browse php folder in windows C-> click php-cgi (if you don't see it there make sure next to file name it says php executable).Then click ok. 
</p>
<br /v
<p>
<img src= https://i.imgur.com/W3gkHKG.png height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next we will install Osticket from the installation files. Go to downloads, then open the file folder "osticket" in a new tab-> next open windows (C:)-> open inetpub-> open wwwroot-> drag folder "uplodad" into wwwroot. Within c:\inetpub\wwwroot, Rename “upload” to “osTicket”.
</p>
<br /v
<p>
<img src= https://i.imgur.com/bm6A0aY.png width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Reload IIS (Open, then click restart). tap sites--> Default web site-->click osticket--> click browse *:80 (http). From here you should be able to see osticket.
</p>
<br /v
<p>
<img src= https://i.imgur.com/7IdcEEQ.png height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
in the last step there were extentions missing, so what we are going to do is enable them. open IIS manager-> click php manager-> click enable or disable an extension-> enable php_imap.dll -> enable php_ intl.dll-> enable php_opache.dll. Referesh osticket and view the changes.
</p>
<br /v
<p>
<img src= https://i.imgur.com/u9JR2cS.png height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next we will rename the following folder from windows c:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php -> windows c:\inetpub\wwwroot\osTicket\include\ost-config.php.
</p>
<br /v
<p>
<img src= https://i.imgur.com/lspMkHR.png height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Right click ost-config.php-> click properties-> click security-> click advanced-> click disable inheritance-> click add then select principle-> type everyone then check names->click ok and make sure you check full permissisonslick check names-> click ok, then apply and  okay again.   
</p>
<br /v
<p>
<img src= https://i.imgur.com/03bIqor.png height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Continue Setting up osTicket in the browser (click continue). Name the helpdesk and setup a deault email address. 
</p>
<br /v
<p>
<img src=https://i.imgur.com/Qy9EKMR.png height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Download and install Heidi SQL from the installation files.Open Heidi SQL, create a new session and use the same password used for my sql username root password, which is Password1.  
</p>
<br /v
<p>
<img src= https://i.imgur.com/uahEe94.png height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
create a database called osTicket, Open heidi Sql. Right click on unamed, then create a new database. Name it osTicket.  
</p>
<br /v
<p>
<img src= https://i.imgur.com/qVtTO1N.png height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In the osTicket browser continue setting it up. My SQL Database: osTicket  My SQL Username: root MySQL Username: root My SQL password: Password1 and click install now. CONGRATS! hopefully it is installed with no errors.
