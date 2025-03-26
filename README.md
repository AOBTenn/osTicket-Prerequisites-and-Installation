<h1>osTicket - Prerequisites and Installation</h1>
<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h2>Discription </h2>

This tutorial outlines the prerequisites and installation of the free help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Computer)
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
- Link to downloads: https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6


<h2>Installation Steps</h2>

1. Create Microsoft Azure Virtual Machine
   Create Resource Group -> Enter Vm name -> Select Region -> *NOTE* Size: Standard at least 2vcps,  8gib memory -> Enter Username and Password -> Image: Windows 10 Pro, version 22H2 -> Check
   License box -> Next -> Next -> Review and Create
   
![image](https://github.com/user-attachments/assets/9cb237c3-6697-484c-9e0f-ee614a364e0d)
![image](https://github.com/user-attachments/assets/8cbff11c-ba51-4a95-8463-b4bc988cc181)
![image](https://github.com/user-attachments/assets/a37a11a0-2111-4a22-a556-4348b22aa72c)
![image](https://github.com/user-attachments/assets/a1707ac4-9016-4e69-a393-fa0f151759e4)
![image](https://github.com/user-attachments/assets/f97859cb-d393-4ea9-83f8-27d4aa721b11)



3. Login  to the osticket-Vm
   Get public Ip address -> Remote Desktop -> Enter Username/Password

![image](https://github.com/user-attachments/assets/ab816d3e-b197-421a-92d4-00c41bdaad49)
![image](https://github.com/user-attachments/assets/6c574e4c-84d4-4f5a-8211-14696f62d759)



4. Within the Vm download "osTicket-installation-Files.zip" -> Unzip to desktop in new folder "osTicket Installation Files" -> Extract

![image](https://github.com/user-attachments/assets/5c76893c-ad5a-4084-966a-66c7fde57ae8)
![image](https://github.com/user-attachments/assets/2b9b48c0-1628-4f82-a3e0-cf4791e331e7)


5. Enable IIS with CGI
   Check for webserver by browsing 127.0.0.1 -> observe error webpage
   Install webserver -> Start -> Control Panel -> Programs -> Programs and Features -> Turn Windows Features on or off -> Check "Internet Information Services" -> Expand -> Check "CGI" -> Ok

6. Rebrowse 127.0.0.1 and observe the default webpage for IIS should load

7. Install PHP Manager
   osTicket Installation Files Folder -> Double click -> Next -> I Agree -> Next -> Agree to Everything

8. Install Rewrite Moduale
   osTicket Installation Files Folder -> Double click -> Accept -> Finish

9. Create PHP directory on C drive
   Rt click File explorer Open C drive file folder -> Create new folder name "PHP" -> osTicket Installation Files Folder -> Rt click -> Broswe to C drive "PHP" folder -> Extract 

10. Install VC_redist.x86.exe
   osTicket Installation Files Folder -> Double click -> Yes

11. Indstall MySQL5.5.62
    osTicket Installation Files Folder -> Double click -> I agree -> Typical -> Install -> Check Launch -> Finish
    
    After Application Launched
    Next -> Standard -> Next -> Under "Modify security Settings" type Unername/Password -> *Save to Notepad* -> Next -> Execute -> Finish

12. Open IIS as Administrator
    In search bar type "IIS", Rt click "IIS" -> Run as administrator

13. Register PHP in IIS
    Open PhP Manager -> Click "Register New PHP Version" -> Browse PHP folder in C drive -> double click "php.cgi" -> OK

14. Reload IIS / Stop and Restart the server
    Rt click "osTicket-vm" -> Stop -> Wait a few seconds -> Rt click "osTicket-vm" -> Start

15. Install osTicket Application
    osTicket Installation Files Folder -> osTicket v1.15.8 -> Rt click -> Extract -> Open ->  copy "Upload" folder -> browse to "c:\inetphp\wwroot" -> Paste -> Rename "osTicket" spelled extactly

16. Reload IIS / Stop and Restart the server
    Rt click "osTicket-vm" -> Stop -> Wait a few seconds -> Rt click "osTicket-vm" -> Start

17. Browse to osTicket
    "osTicket-vm" -> Sites -> Default Web Site -> osTicket -> Browse *80 -> The osTicket website should load

18. Enable some features that are not orginally enabled at installation
    In IIS -> Default website -> osTicket -> double click PHP manager -> Enable or disable eextensions -> "php_imp.dll, php_inti.dll, php_opcache.dll, Switch to enable -> Refresh osTicket browser

19. Rename "c:\intetpub\wwwroot\osTicket\include\ostsampleconfig.php" to "c:\intetpub\wwwroot\osTicket\include\ost-config.php"
    File Explore -> C drive -> inetpub -> wwwroot -> osTicket -> include -> ostsampleconfig.php -> Rt click -> Rename

20. Assgin permission to "ost-config.php"
    Rt click -> Properties -> Security -> Advanced -> Disable Inheritance -> Remave All -> Add -> Under "Enter the object name..." type "everyone" -> Check names -> Ok -> Full control -> Apply -> Ok

21. Finsih setting up osTicket
    osTicket browser -> Continue -> Enter Help Desk Name -> Enter email address -> Enter admin user -> Enter admin email (differnt from previouly entered email) -> Enter Username/password -> Save credintials to notepad

22. Install Heidi SQL *Create a database specifically for osTicket*
    osTicket Installation Files Folder -> Heidi SQL -> I accept... -> Next four times -> Install -> *Make sure Launch is checked* -> Finish ->

    After Application Launched
    Skip -> New  -> Enter User/Password (same as setting up MySQL) -> Open/Connect to Database -> Rt "Unnamed" -> Create New -> Database -> Type "osTicket" spelled extactly in "Name" -> Ok

23. Finsih setting up osTicket "Database settings"
    osTicket browser ->  Under "MySQL Database" type "osTicket" (database created in previous step) ->  Under "MySQL Username" enter username (same as setting up MySQL) ->  Under "MySQL Password" enter password (same as setting up MySQL) -> Install Now

Congratulations. If you followed these steps exactly you have successfully installed the free ticketing software osTicket. Now you can continue to practicing creating and solving simulated real  world Help desK tickets.
