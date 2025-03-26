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

2. Login  to the osticket-Vm
   Get public Ip address -> Remote Desktop -> Enter Username/Password

3. Within the Vm download "osTicket-installation-Files.zip" -> Unzip to desktop in new folder "osTicket Installation Files" -> Extract

4. Enable IIS with CGI
   Check for webserver by browsing 127.0.0.1 -> observe error webpage
   Install webserver -> Start -> Control Panel -> Programs -> Programs and Features -> Turn Windows Features on or off -> Check "Internet Information Services" -> Expand -> Check "CGI" -> Ok

5. Rebrowse 127.0.0.1 and observe the default webpage for IIS should load

6. Install PHP Manager
   osTicket Installation Files Folder -> Double click -> Next -> I Agree -> Next -> Agree to Everything

7. Install Rewrite Moduale
   osTicket Installation Files Folder -> Double click -> Accept -> Finish

8. Create PHP directory on C drive
   Rt click File explorer Open C drive file folder -> Create new folder name "PHP" -> osTicket Installation Files Folder -> Rt click -> Broswe to C drive "PHP" folder -> Extract 

9. Install VC_redist.x86.exe
   osTicket Installation Files Folder -> Double click -> Yes

10. Indstall MySQL5.5.62
    osTicket Installation Files Folder -> Double click -> I agree -> Typical -> Install -> Check Launch -> Finish
    
    After Application Launched
    Next -> Standard -> Next -> Under "Modify security Settings" type Unername/Password -> *Save to Notepad* -> Next -> Execute -> Finish

11. Open IIS as Administrator
    In search bar type "IIS", Rt click "IIS" -> Run as administrator

12. Register PHP in IIS
    Open PhP Manager -> Click "Register New PHP Version" -> Browse PHP folder in C drive -> double click "php.cgi" -> OK

13. Reload IIS / Stop and Restart the server
    Rt click "osTicket-vm" -> Stop -> Wait a few seconds -> Rt click "osTicket-vm" -> Start

14. Install osTicket Application
    osTicket Installation Files Folder -> osTicket v1.15.8 -> Rt click -> Extract -> Open ->  copy "Upload" folder -> browse to "c:\inetphp\wwroot" -> Paste -> Rename "osTicket" spelled extactly

15. Reload IIS / Stop and Restart the server
    Rt click "osTicket-vm" -> Stop -> Wait a few seconds -> Rt click "osTicket-vm" -> Start

16. Browse to osTicket
    "osTicket-vm" -> Sites -> Default Web Site -> osTicket -> Browse *80 -> The osTicket website should load

17. Enable some features that are not orginally enabled at installation
    In IIS -> Default website -> osTicket -> double click PHP manager -> Enable or disable eextensions -> "php_imp.dll, php_inti.dll, php_opcache.dll, Switch to enable -> Refresh osTicket browser

18. Rename "c:\intetpub\wwwroot\osTicket\include\ostsampleconfig.php" to "c:\intetpub\wwwroot\osTicket\include\ost-config.php"
    File Explore -> C drive -> inetpub -> wwwroot -> osTicket -> include -> ostsampleconfig.php -> Rt click -> Rename

19. Assgin permission to "ost-config.php"
    Rt click -> Properties -> Security -> Advanced -> Disable Inheritance -> Remave All -> Add -> Under "Enter the object name..." type "everyone" -> Check names -> Ok -> Full control -> Apply -> Ok

20. Finsih setting up osTicket
    osTicket browser -> Continue -> Enter Help Desk Name -> Enter email address -> Enter admin user -> Enter admin email (differnt from previouly entered email) -> Enter Username/password -> Save credintials to notepad

21. Install Heidi SQL *Create a database specifically for osTicket*
    osTicket Installation Files Folder -> Heidi SQL -> I accept... -> Next four times -> Install -> *Make sure Launch is checked* -> Finish ->

    After Application Launched
    Skip -> New  -> Enter User/Password (same as setting up MySQL) -> Open/Connect to Database -> Rt "Unnamed" -> Create New -> Database -> Type "osTicket" spelled extactly in "Name" -> Ok

22. Finsih setting up osTicket "Database settings"
    osTicket browser ->  Under "MySQL Database" type "osTicket" (database created in previous step) ->  Under "MySQL Username" enter username (same as setting up MySQL) ->  Under "MySQL Password" enter password (same as setting up MySQL) -> Install Now

Congratulations. If you followed these steps exactly you have successfully installed the free ticketing software osTicket. Now you can continue to practicing creating and solving simulated real  world Help desK tickets.
