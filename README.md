<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
In this tutorial, we cover the prerequisites and installation process for osTicket, an open-source ticketing platform.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop Connection
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- IIS
- PHP Manager
- VC_redistx86
- MySQL 5.5.62
- Rewrite Module
- Heidi SQL

<h2>Installation Steps</h2>
<h2>Setting up osTicket in Azure VM</h2>

1. <strong>Create Virtual Machine in Azure:</strong>
- <strong>Log into Azure Portal</strong>
- <strong>Create a new VM with Windows Server.</strong>
<p>
In Microsoft Azure, I created a virtual machine named osTicket-vm, which is running Windows pro 10.
</p>
<p>
<img src="https://i.imgur.com/nBoVDkW.png" width="600" alt="Disk Sanitization Steps"/>
</p>

<br />

<p>
- Use the VM’s public IP address to establish a connection through Remote Desktop Protocol (RDP). Start > type mstsc click on remote desktop > paste public IP address and log in with credentials you made when you created the VM (bluemachina in this example).
</p>
<p>
<img src="https://i.imgur.com/DtLvxn1.png" width="600" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/LSnti05.png" width="600" alt="Disk Sanitization Steps"/>
</p>

<br />

<strong>2. Download the osTicket-installation-Files.zip</strong>
<p>
- Within your VM, download the file from https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD and extract the contents to your desktop. These files will be used to install osTicket.
  <img src="https://i.imgur.com/sLqGSgr.png" width="600" alt="Disk Sanitization Steps"/>
</p>

<strong> 3. Enable ISS with CGI </strong>
<p>
- Open the Control Panel > navigate to Programs > Programs and Features > then select Turn Windows features on or off.
   <img src="https://i.imgur.com/WZkgTI8.png" width="600" alt="Disk Sanitization Steps"/>
</p>
<br />

- <strong> Enable (internet information services) World Wide Web Services > Application Development Features > enable CGI </strong>
<p>
  <img src="https://i.imgur.com/jpdP5dP.png" width="600" alt="Disk Sanitization Steps"/>
</p>
</p>
<br />

<strong> 4. Download and Install PHP manager from the osTicket-installation-Files </strong>
<p>
  - Install from the osTicket-installation-Files (PHPManagerForIIS_V1.5.0.msi) PHP is basically a backend web server language and osTicket runs on PHP.
</p>
<p>
  <img src="https://i.imgur.com/wkNBoFU.png" width="600" alt="Disk Sanitization Steps"/>
</p>
<br />

<strong> 5. Download and Install the Rewrite Module</strong>
<p>
  - Install (rewrite_amd64_en-US.msi) from the osTicket-Installation-Files
  <img src="https://i.imgur.com/GDmo2tA.png" width="600" alt="Disk Sanitization Steps"/>
</p>
<br />

<strong> 6. Create a directory in the C drive. Name the folder PHP. </strong>
<p>
  <img src="https://i.imgur.com/KqLeICV.png" width="600" alt="Disk Sanitization Steps"/>
</p>
<br />

<strong> 7. From the osTicket-Installation-Files install (php-7.3.8-nts-Win32-VC15-x86.zip) into C:\PHP </strong>
<p>
  <img src="https://i.imgur.com/ia4JD6X.png" width="600" alt="Disk Sanitization Steps"/>
</p>
<br />

<strong> 8. Download and Install the (VC_redist.x86.exe) </strong>
- Install from the osTicket-Installation-Files
<p>
  <img src="https://i.imgur.com/XXx1V0d.png" width="600" alt="Disk Sanitization Steps"/>
</p>
<br />

<strong> 9. Download and Install MySQL 5.5.62 (mysql-5.5.62-win32.msi)</strong>
- Install from the osTicket-Installation-Files
- Select the following configurations:
     - Typical setup
     - launch configuration
     - Standard configuration
<p>
  <img src="https://i.imgur.com/ImnzCOT.png" width="600" alt="Disk Sanitization Steps"/>
</p>
<br />

- <strong>  The user for this service is going to type (root) as the username and the password.</strong>

<p>
  <img src="https://i.imgur.com/9w5ButR.png" width="600" alt="Disk Sanitization Steps"/>
</p>
<br />

<strong> 10. Launch IIS as administrator </strong>
- Search for IIS in the windows search bar and right click it and select open as administrator
<p>
  <img src="https://i.imgur.com/VDqcIuc.png" width="600" alt="Disk Sanitization Steps"/>
</p>
<br />

<strong> 11. Register PHP from within IIS </strong>
- Open the PHP manager
- Register new PHP version
<p>
  <img src="https://i.imgur.com/cM6mFZd.png" width="600" alt="Disk Sanitization Steps"/>
</p>
<p>
  - browse(...) > Go to your C drive > PHP folder > php.cgi
</p>
<p>
  <img src="https://i.imgur.com/0tXdSfb.png" width="600" alt="Disk Sanitization Steps"/>
</p> 
<br />

<strong> 12. Reload IIS (Open ISS, Stop and Start the server) </strong>
- The restart button can be found on the right sider of the window
<p>
  <img src="https://i.imgur.com/dfQQkom.png" width="600" alt="Disk Sanitization Steps"/>
</p>
<br />

<strong> 13. Download and install osTicket</strong>
- From the osTicket-Installation-Files unzip the (osTicketv1.15.8)
<p>
  <img src="https://i.imgur.com/YG90QsC.png" width="600" alt="Disk Sanitization Steps"/>
</p>
<p>
  - After extracting the folder, click on the folder and then copy the "upload" folder into "c: inetpub\wwwroot"
    - open file explorer > C drive > inetpub > wwwroot
</p>
  <img src="https://i.imgur.com/TU2Jsj5.png" width="600" alt="Disk Sanitization Steps"/>

  - Within "c: inetpub\wwwroot", Rename "upload" to "osTicket"

  <img src="https://i.imgur.com/iRaAcrD.png" width="600" alt="Disk Sanitization Steps"/>
  <br />

<strong> 14. Reload IIS (Open ISS, Stop and Start the server) </strong>
- The restart button can be found on the right sider of the window
<p>
  <img src="https://i.imgur.com/bUKnGlQ.png" width="600" alt="Disk Sanitization Steps"/>
</p>
<br />

<strong> 15. Launch osTicket </strong>
- On the left hand side of IIS, Expand on the VM name > Sites > Default Website > osTicket
- click on the browse *:80(http)
<p>
  <img src="https://i.imgur.com/eG8T47L.png" width="600" alt="Disk Sanitization Steps"/>
</p>
<p>
  - Your web browser will open and display osTicket.
</p>
<img src="https://i.imgur.com/HluqtJz.png" width="600" alt="Disk Sanitization Steps"/>
<br />

<strong> 16. Enable extensions </strong>
- open IIS > sites > Default > osTicket
- Double-click PHP manager
<p>
  <img src="https://i.imgur.com/yDGZ20K.png" width="600" alt="Disk Sanitization Steps"/>
</p>
<p>
  - Click "Enable or disable an extension"

 - Enable: php_imap.dll
 - Enable: php_intl.dll
 - Enable: php_opache.dll
</p>
<img src="https://i.imgur.com/5qRzGLs.png" width="600" alt="Disk Sanitization Steps"/>
<br />

<strong> 17. Refresh osTicket </strong>
- Refresh the osTicket site in your browser, some extensions will now appear active
<p>
  <img src="https://i.imgur.com/8BAJSmv.png" width="600" alt="Disk Sanitization Steps"/>
</p>
<br />

<strong> 18. Change to ost-config.ph </strong>
- Rename: ost-config.php
- From: C:\inetpub|wwwrootlosTicket\includelost-sampleconfig.php
-To: C. linetpubiwwwrootlos Ticketinclude lost-config.php
- rename "ost-sampleconfig.ph" to "ost-config.ph"
<p>
  <img src="https://i.imgur.com/zABTjKT.png" width="600" alt="Disk Sanitization Steps"/>
</p>
<br />

<strong> 19. Change ost-config.ph permissions </strong>
- Change ost-config.php permissions by right clicking and selecting
- Properties > Security > Advance > Disable inheritance
- Disable inhertiance > Remove All
<p>
  <img src="https://i.imgur.com/Wvke8Jx.png" width="600" alt="Disk Sanitization Steps"/>
</p>
- New Permissions > Everyone > All
-Go to add > select prinicpal > Everyone > Clcik full access > apply > OK
<p>
   <img src="https://i.imgur.com/A8dSkh8.png" width="600" alt="Disk Sanitization Steps"/>
</p>
<br />

<strong> 20. Continue osTicket installation</strong>
- Continue the osTicket installer on your browser by filling the first half of the page
<p>
  <img src="https://i.imgur.com/JxKYD9S.png" width="600" alt="Disk Sanitization Steps"/>
</p>
<br />

<strong> 21. Download and install Heidi SQL from the osTicket-Installation-Files </strong>
<p>
  <img src="https://i.imgur.com/INRtwOT.png" width="600" alt="Disk Sanitization Steps"/>
</p>
- Open Heidi SQL and create a new version a new session > Fill in username and password as (root) > Then click open
<p>
  <img src="https://i.imgur.com/s4TZXLh.png" width="600" alt="Disk Sanitization Steps"/>
</p>
<br />

<strong> 22. Create new database </strong>
- On the left side of the window, right click on "Unnamed" and click create new database and name it "osTicket"
<p>
  <img src="https://i.imgur.com/BGNDvMg.png" width="600" alt="Disk Sanitization Steps"/>
</p>
<br />

<strong> 23. Finish signing in database settings </strong>
- Then go back to your osTicket browser and fill up the missing credentials
- Install Now
<p>
  <img src="https://i.imgur.com/21UDFIl.png" width="600" alt="Disk Sanitization Steps"/>
</p>
<br />

<strong> 24. Finalize osTicket installation</strong>
<p>
  <img src="https://i.imgur.com/42cOzxz.png" width="600" alt="Disk Sanitization Steps"/>
</p>
<br />
