<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Installation and Configuration</h1>
This tutorial outlines the installation and configuration of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Installation Steps</h2>

</p>
<p>
Create an Azure Virtual Machine<br/> 
- Create a new Virtual Machine using a new Resource Group<br/> 
- Select your preferred Region and Availability Zone<br/>
- On the Image and Size tab, choose an efficient OS for your business needs
<br />

![image](https://github.com/user-attachments/assets/027be1e3-1949-4983-bd1b-703f225a7953)

</p>
<p>
Open Remote Desktop Connection and login using your credentials
<br />
  
![image](https://github.com/user-attachments/assets/9a8264b8-7946-4068-87e1-d61794700c8b)

To install and Enable IIS in Windows, press the Windows key and search "Turn on Windows features on or off"

![Screenshot 2025-05-13 192024](https://github.com/user-attachments/assets/e730d8f3-752f-40a0-b7b7-2f22d73200e6)

</p>
<p>
Enable/Check Internet Information Services<br />

![image](https://github.com/user-attachments/assets/7202ce8b-18d1-4cf6-b417-c3fb9a1bbe3e)  

To enable CGI, on the same IIS folder, expand to World Wide Web Services > Application Development Features > then Check CGI

![image](https://github.com/user-attachments/assets/f9060745-4dac-4573-a685-4bebc7e372ba)

With the following files, do the following
-Install PHP Manager for IIS<br />
-Install Rewrite Module<br />
-Create a directory C:\PHP and unzp the PHP 7.3.8 to that folder<br />
-Install VC Redist<br />
-Install MySQL 5.5.62<br />



</p>
<p>
</p>
<br />
