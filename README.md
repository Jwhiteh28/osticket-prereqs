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
