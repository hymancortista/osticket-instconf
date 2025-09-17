<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Installation of osTicket</h1>
This tutorial outlines the installation of the open-source help desk ticketing system osTicket.<br />

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

Using this link, download and extract these files necessary for our setup<br />
- Install PHP Manager for IIS<br />
<img width="492" height="401" alt="image" src="https://github.com/user-attachments/assets/318b169f-555a-4a18-8b37-df8e919c76dd" />

- Install Rewrite Module<br />
<img width="486" height="375" alt="image" src="https://github.com/user-attachments/assets/a6510a3f-b464-4f56-8507-3adcc8c52b76" />

- Create a directory C:\PHP and unzip the PHP 7.3.8 to that folder<br />
<img width="1113" height="628" alt="image" src="https://github.com/user-attachments/assets/379253c8-01d9-4212-bc30-1d6865b453b4" />

- Install VC Redist<br />
<img width="470" height="286" alt="image" src="https://github.com/user-attachments/assets/324b89d2-4ff1-4c6b-b0fa-08c00008a4bc" />

- Install MySQL 5.5.62<br />
<img width="486" height="376" alt="image" src="https://github.com/user-attachments/assets/32057622-3ea4-46e1-b487-ffeaa44c4f18" />


Do the following
- Open IIS as Admin
<img width="775" height="611" alt="image" src="https://github.com/user-attachments/assets/ef42ca00-f9d9-4b3d-8365-53a12215d8ff" />

- Register PHP from within IIS using 'php-cgi' from the PHP folder
<img width="746" height="607" alt="image" src="https://github.com/user-attachments/assets/a1620569-49f3-40ed-9c99-79b073d4c246" />


- Extract the osTicket folder and transfer "upload" to “c:\inetpub\wwwroot”
- Within “c:\inetpub\wwwroot”, Rename “upload” to “osTicket”
<img width="881" height="392" alt="image" src="https://github.com/user-attachments/assets/cce9d401-bb78-4a37-8cd7-422de1240400" />

- Reload IIS (Stop and Start the server)

Go back to IIS, sites > Default > osTicket
- Double click PHP Manager
- Enable php_imap.dll
- Enable php_intl.dll
- Enable php_opcache.dll
<img width="712" height="460" alt="image" src="https://github.com/user-attachments/assets/2c1a08b0-297c-4f4e-a873-0dff84a756f3" />


From C:\inetpub\wwwroot\osTicket\include
- Rename ost-sampleconfig.php to ost-config.php
- Right click on ost-config.php then click Properties
- Disable Inheritance
<img width="758" height="512" alt="image" src="https://github.com/user-attachments/assets/0a9f484a-fb46-4968-8204-afe663502192" />

- Click Add > Everyone > Full Control
- Click Apply > OK
<img width="902" height="586" alt="image" src="https://github.com/user-attachments/assets/6e8798a1-4091-49e7-8e06-93e54242f038" />


Within IIS, Go to sites -> Default -> osTicket
On the right, click “Browse *:80” -> Continue <br/>

Fill out your information <br/>
![image](https://github.com/user-attachments/assets/3a556260-b14e-4e02-b33f-5aefd814e6a2)

From the “osTicket-Installation-Files” folder, install HeidiSQL.
- Open Heidi SQL
- Create a new session, root/root
- Connect to the session

![image](https://github.com/user-attachments/assets/b7bd0d04-eb73-4185-8651-f7d93dae011d)

Create a database called “osTicket”

![image](https://github.com/user-attachments/assets/8b210989-35e8-451f-af7d-a6386ed32fcb)


Continue Setting up osTicket in the browser
- MySQL Database: osTicket
- MySQL Username: root
- MySQL Password: root
- Click “Install Now!”

<img width="833" height="653" alt="image" src="https://github.com/user-attachments/assets/10a5a14a-606b-4958-8720-5cb89602ef5e" />

It is now installed, now we can proceed to next step which is to Configure osTicket




