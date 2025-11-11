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

- Azure subscription and Virtual Machine 
- osTicket installation files 
- Enable IIS and CGI
- Install PHP manager
- Install the Rewrite Module
- Create a directory for PHP 
- Install VC redist
- Install MYSQL
- Install HeidiSQL

<h2>Installation Steps</h2>
Welcome to my first in-depth IT tutorial! To begin this lab, you first have to create a virtual machine using the free trial of Microsoft Azure (https://azure.microsoft.com). We will be using a VM (virtual machine), which is a remote computer on a server. We are using a VM in order to safely run different operating systems on one computer and to test software in a safe environment. When you create the VM, name it osticket-vm and the username labuser with the password as osTicketPassword1! Afterwards, for the image use Windows 10 with about 2-4 CPUs. In this example, I will be using 4 CPUs.


<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, simply connect to your VM you just created using RDP (remote desktop protocol) using the IPV4 address of the VM and enter labuser for the username and osTicketPassword1! for the password. If you're using a Mac, you have to download Microsoft RDP from the App Store.
 
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now open Microsoft Edge in the VM and paste this link in the address bar, and once opened, download the link. That link will provide you with the osTicket installation files. https://docs.google.com/document/d/1Y5j7aml8LVDBH7Ne5szGkyX-FL3aLdeT5a2UAsFAesg/edit?tab=t.0 
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Afterwards, go to the start menu and open Control Panel by searching for it. Then look for programs and select the uninstall program link. After that, select the Turn Windows Features On and Off link, and check off IIS ( Internet Information Services) in the list and expand it. Then expand World Wide Web Services, and expand Application Development Features right after that, check off CGI, and select ok.
</p>
<br />
