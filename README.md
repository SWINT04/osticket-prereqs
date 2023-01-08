<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

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
Hello and welcome, I will show you how to install Osticket. First we will be creating a Virtual machine using the Microsoft Azure portal. We will be using a VM which is a remote computer. We are using a VM in order to create space and manage operating sysmtems. Next we will Create a resource group and name it "Rg-osTicket". Then we will create a VM with 2 or 4 CPUs. In the example above I will be using 4 CPUs.
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
