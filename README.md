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
Welcome to my first in-depth IT tutorial! To begin this lab, you first have to create a virtual machine using the free trial of Microsoft Azure (https://azure.microsoft.com). We will be using a VM (virtual machine), which is a remote computer on a server. We are using a VM to run different operating systems on one computer safely and to test software in a safe environment. When you create the VM, name the resource group osticket and VM name osticket-vm, and set the region to East US 2. Then set the username to labuser with the password as osTicketPassword1!. Afterwards, for the image use Windows 10 with about 2-4 CPUs. In this example, I will be using 4 CPUs.


<p>
<img width="2558" height="1308" alt="image" src="https://github.com/user-attachments/assets/a503b7ee-7ee1-49f1-a166-5ba66943d6ca" />
</p>
<p>
Next, simply connect to your VM you just created using RDP (remote desktop protocol) using the IPV4 address of the VM and enter labuser for the username and osTicketPassword1! for the password. If you're using a Mac, you have to download Microsoft RDP from the App Store.
 
</p>
<br />

<p>
<img width="871" height="235" alt="image" src="https://github.com/user-attachments/assets/439f3083-1fed-4c0c-aca6-ea40a34654f5" />
</p>
<p>
Now open Microsoft Edge in the VM and paste this link in the address bar, and once opened, download the link. That link will provide you with the osTicket installation files. https://docs.google.com/document/d/1Y5j7aml8LVDBH7Ne5szGkyX-FL3aLdeT5a2UAsFAesg/edit?tab=t.0 Once the folder is downloaded, put the folder onto the desktop, unzip the folder, and put the original download zip folder in the trash since you will no longer need it. 

</p>
<br />

<p>
<img width="735" height="493" alt="image" src="https://github.com/user-attachments/assets/5921f937-8e32-4461-bea1-2dea080a795a" />
</p>
<p>
Afterwards, go to the start menu and open Control Panel by searching for it. Then look for programs and select the uninstall program link. After that, select the Turn Windows Features On and Off link, and check IIS ( Internet Information Services) in the list and expand it. Then expand World Wide Web Services, and expand Application Development Features right after that, check CGI, and select ok.

</p>
<br />

<p>
<img width="1245" height="715" alt="image" src="https://github.com/user-attachments/assets/88add05b-0b0d-49a0-926c-ed54ebb448a9" />
</p>
<p>
 Now, open the osTicket installation files folder and install the PHP Manager for IIS. And from the same folder, install the Rewrite Module.

</p>
<br />

<p>
<img width="501" height="416" alt="image" src="https://github.com/user-attachments/assets/128aeeaa-df94-4183-92bb-7c30a5775650" />
</p>
<p>
Next, you have to create a folder named PHP within the (C:) drive of the VM. Then, from the osTicket-Installation-Files folder, unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder you just created.

</p>
<br />

<p>
<img width="1185" height="712" alt="image" src="https://github.com/user-attachments/assets/a111bcf0-67a5-4d39-b537-9a9ce57cbdeb" />
</p>
<p>
Then, from the osTicket-Installation-Files folder, install VC_redist.x86.exe and MySQL 5.5.62. When you're installing MySQL server, select Typical for Choose My Setup type and then Install and select the option to launch MySQL.

</p>
<br />

<p>
<img width="1628" height="664" alt="image" src="https://github.com/user-attachments/assets/86e68498-d1e5-49e2-b7c8-d4d829d3a54d" /> 
</p>
<p>
Once MySQL is launched, click Next and select Standard Configuration, then click Next again. Afterwards, hit next for the third window and for the username and password, set it as root for both and select next, and then execute.

</p>
<br />

<p>
<img width="515" height="394" alt="image" src="https://github.com/user-attachments/assets/3aa7098e-c05e-4ec4-8794-849b598dc975" />
</p>
<p>
Now open IIS as an Admin from the Start menu by searching for it. Within IIS, select the PHP manager icon and then select the Register New PHP version link. Now, within the pop-up, click on the three dots on the right to browse the file explorer and select the PHP Folder you created in the (C:) drive, select php-cgi.exe, and select ok. Next, go back to IIS Manager and stop and start the server.

</p>
<br />

<p>
<img width="1908" height="1024" alt="image" src="https://github.com/user-attachments/assets/705d09ce-5063-467b-9cfa-7cbab7e2c861" />
</p>
<p>
After that, from the osTicket- Installation files folder, unzip “osTicket-v1.15.8.zip” and paste the “upload” folder into “c:\inetpub\wwwroot” and within “c:\inetpub\wwwroot”, rename upload to osTicket exactly how it's written here. Now, once again, open IIS Manager as an administrator if you closed the program, and stop and start the server to restart it.

</p>
<br />

<p>
<img width="1128" height="636" alt="image" src="https://github.com/user-attachments/assets/99d041a0-6ca3-4371-8e7b-cd87f6aad7ce" />
</p>
<p>
Furthermore, go back to IIS and go to sites -> Default -> osTicket. On the right, after you click osTicket, click “Browse *:80”. Then go back to IIS, sites -> Default -> osTicket Double-click PHP Manager Click “Enable or disable an extension” Enable: php_imap.dll, Enable: php_intl.dll, and Enable: php_opcache. Refresh the osTicket site in your browser, and observe the changes.

</p>
<br />

<p>
<img width="2556" height="1372" alt="image" src="https://github.com/user-attachments/assets/1797fa6a-f19e-4e77-8f19-038aedff7933" />
</p>
<p>
Next, open up File Explorer, go to the (C:) drive -> inetpub -> wwwwroot -> osTicket -> include -> ost-sampleconfig.php, and rename it to ost-config.php exactly like how it's written. Then right-click ost-config.php and select properties -> security -> advanced, and select Disable inheritance -> remove all -> principal -> Everyone -> Full Control -> apply -> OK

</p>
<br />

<p>
<img width="766" height="521" alt="image" src="https://github.com/user-attachments/assets/6c792738-594c-4bf4-9193-709311308abe" />
</p>
<p>
Continue setting up osTicket in the browser (click Continue). Put down whatever you want for the helpdesk name and default email. Then, for the Username, put adminuser, and for the password, put Password1, but you're not done yet, so don't hit install.

</p>
<br />

<p>
<img width="2560" height="1407" alt="image" src="https://github.com/user-attachments/assets/77cb2127-0392-403c-87c9-fdb673228c4f" /> 
</p>
<p>
From the “osTicket-Installation-Files” folder, install HeidiSQL. Open Heidi SQL, create a new session, set root/root for username and password, connect to the session, and create a database called “osTicket”.

</p>
<br />

<p>
<img width="1729" height="636" alt="image" src="https://github.com/user-attachments/assets/c5c012f8-21d0-4ef3-8457-21bde939bce1" />
</p>
<p>
Continue setting up osTicket in the browser. MySQL Database: osTicket, Username: root, Password: root, Click “Install Now!”. Congratulations, hopefully it is installed with no errors!

</p>
<br />

<p>
<img width="2560" height="1399" alt="image" src="https://github.com/user-attachments/assets/7c7766de-3be7-41f9-a4eb-2913b5e67783" />

