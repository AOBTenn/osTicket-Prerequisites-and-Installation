
<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />



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

2. Remote Desktop Login  to the Vm
   Get public Ip address -> Enter Username and Password

3. Within the Vm download "osTicket-installation-Files.zip" -> Unzip to desktop in new folder "osTicket Installation Files" -> Extract

4. Enable IIS with CGI
   Check for webserver by browsing 127.0.0.1 ->
   Install webserver -> Start -> Control Panel -> Programs -> Programs and Features -> Turn Windows Features on or off -> Check "Internet Information Services" -> Expand -> Check "CGI" -> Ok

5. Rebrowse 127.0.0.1 and observe the default webpage for IIS should load

6. Install PHP Manager
   osTicket Installation Files Folder -> Double click -> Next -> I Agree -> Next -> Agree to Everything

7. Install Rewrite Moduale
   osTicket Installation Files Folder -> Double click -> Accept -> Finish

8.  Create PHP directory on C drive
   Open C drive file folder -> Create new folder name "PHP" -> osTicket Installation Files Folder -> Rt click -> Extract into C drive "PHP" folder

9.


