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
- Internet Information Services (IIS)
- PHP Manager
- Rewrite Module
- VC Redist
- MySQL
- Heidi SQL
- osTicket v1.15.8

<h2>Installation Steps</h2>

<p>
<img width="1728" alt="9A58B889-243B-49B1-B493-3B069A4B4553" src="https://github.com/user-attachments/assets/a5b78147-0425-40a7-9102-32c0087c889e" />


<p>
Create a Windows 10 VM in Azure named osticket-vm (4 vCPUs, username: labuser, password: osTicketPassword1!) and log in via Remote Desktop. Inside the VM, unzip the osTicket-Installation-Files.zip to your desktop.
</p>
<br />

<p>
<img width="1728" alt="19ED2EFE-C2F4-4BE9-9F44-FF24490D445D" src="https://github.com/user-attachments/assets/162c2e51-bc66-45f9-ab3a-b69bad2d5a61" />

</p>
<p>

Install and enable IIS with CGI, PHP Manager, Rewrite Module, and unzip PHP 7.3.8 to C:\PHP. Install VC_redist, MySQL 5.5.62 (root/root), and register PHP in IIS using PHP Manager.


</p>
<br />

<p>
  
![image](https://github.com/user-attachments/assets/48b55380-5579-4787-baf2-3d9f979901b1)

</p>
<p>
Unzip osTicket v1.15.8 to C:\inetpub\wwwroot\osTicket, then restart IIS and browse the site. Enable required PHP extensions (imap, intl, opcache) in PHP Manager. Rename ost-sampleconfig.php to ost-config.php, set full permissions for "Everyone", and proceed with the browser setup. </p>

![12E8DC6E-3B2B-4956-9542-F19F2AA5FED0_1_105_c](https://github.com/user-attachments/assets/602493b9-b9be-48bb-859a-2705afda8a33)


Create the osTicket database in HeidiSQL, complete the install with MySQL credentials (root/root), and finish setup at http://localhost/osTicket/. Finally, delete the setup folder and set ost-config.php to read-only.




