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
 <p> 
</p>

Create Resource Group -> Enter Vm name -> Select Region -> *NOTE* Size: Standard at least 2vcps,  8gib memory -> Enter Username and Password -> Image: Windows 10 Pro, version 22H2 -> Check License box -> Next -> Next -> Review and Create
    <p> 
</p>

![image](https://github.com/user-attachments/assets/9cb237c3-6697-484c-9e0f-ee614a364e0d)
 <p> 
</p>

![image](https://github.com/user-attachments/assets/8cbff11c-ba51-4a95-8463-b4bc988cc181)
 <p> 
</p>

![image](https://github.com/user-attachments/assets/a37a11a0-2111-4a22-a556-4348b22aa72c)
 <p> 
</p>

![image](https://github.com/user-attachments/assets/a1707ac4-9016-4e69-a393-fa0f151759e4)
 <p> 
</p>

![image](https://github.com/user-attachments/assets/f97859cb-d393-4ea9-83f8-27d4aa721b11)
 <p> 
</p>

3. Login  to the osticket-Vm
    <p> 
</p>

 Get public Ip address -> Remote Desktop -> Enter Username/Password
 <p> 
</p>

![image](https://github.com/user-attachments/assets/7cfc5936-8abf-407e-b10b-f896f5d0c434)
 <p> 
</p>

![image](https://github.com/user-attachments/assets/6c574e4c-84d4-4f5a-8211-14696f62d759)
 <p> 
</p>

4. Within the Vm download "osTicket-installation-Files.zip" -> Unzip to desktop in new folder "osTicket Installation Files" -> Extract
 <p> 
</p>

![image](https://github.com/user-attachments/assets/41c20a8d-68d0-4e3a-a47c-465ce2c7efa3)
 <p> 
</p>

![image](https://github.com/user-attachments/assets/2b9b48c0-1628-4f82-a3e0-cf4791e331e7)
 <p> 
</p>

5. Enable IIS with CGI
 <p> 
</p>

Check for webserver by browsing 127.0.0.1 -> observe error webpage
   <p> 
</p>

![image](https://github.com/user-attachments/assets/242180c7-4e08-4557-87a5-a6e4ffcbf56c)
 <p> 
</p>

![image](https://github.com/user-attachments/assets/75955188-d47a-4df2-a7a7-1fa7f10efbd7)
 <p> 
</p>

6. Install webserver 
    <p> 
</p>

Start -> Control Panel -> Programs -> Programs and Features -> Turn Windows Features on or off -> Check "Internet Information Services" -> Expand -> Check "CGI" -> Ok
 <p> 
</p>

![image](https://github.com/user-attachments/assets/9682ce29-751a-4c25-92c4-07a44768fb87)
 <p> 
</p>

![image](https://github.com/user-attachments/assets/dd1313e4-8ba1-4d7c-b7b0-ff18146fb9ae)
 <p> 
</p>

![image](https://github.com/user-attachments/assets/90784a04-9528-4d19-a171-c07a1ccfaad2)
 <p> 
</p>

![image](https://github.com/user-attachments/assets/712f041a-5986-4d88-9bec-20c2abfa6d90)
 <p> 
</p>

7. Rebrowse 127.0.0.1 and observe the default webpage for IIS should load
 <p> 
</p>

![image](https://github.com/user-attachments/assets/8d5ecd8d-88db-4a4e-8d15-53b6a050e509)
 <p> 
</p>

8. Install PHP Manager
 <p> 
</p>

osTicket Installation Files Folder -> Double click -> Next -> I Agree -> Next -> Agree to Everything
 <p> 
</p>

![image](https://github.com/user-attachments/assets/bae74334-e962-46e5-b3f7-eaf0764d04f4)
 <p> 
</p>

![image](https://github.com/user-attachments/assets/8d7f46f6-9070-4c66-9e75-e375dba156ac)
 <p> 
</p>

9. Install Rewrite Moduale
 <p> 
</p>

osTicket Installation Files Folder -> Double click -> Accept -> Finish
 <p> 
</p>

![image](https://github.com/user-attachments/assets/1ae9065b-ec0c-4594-a79e-ac671b0a9c4a)
 <p> 
</p>

![image](https://github.com/user-attachments/assets/8b3a1f5c-6427-4bc4-9167-60f164096a3e)
 <p> 
</p>

10. Create PHP directory on C drive
 <p> 
</p>

Rt click File explorer Open C drive file folder -> Create new folder name "PHP"
 <p> 
</p>

![image](https://github.com/user-attachments/assets/63e01625-8348-436e-ad78-f6e4cedcd095)
 <p> 
</p>

11. Unzip PHP in osTicket Installation Files Folder into PHP on C drive
 <p> 
</p>

osTicket Installation Files Folder -> -> Rt click -> Broswe to C drive "PHP" folder -> Extract 
 <p> 
</p>

![image](https://github.com/user-attachments/assets/7e2dbc54-5698-4095-ac2c-dcd4a55d9368)
 <p> 
</p>

![image](https://github.com/user-attachments/assets/9d4361ec-36d4-41cc-9c10-93dfb6b08355)
 <p> 
</p>

12. Install VC_redist.x86.exe
 <p> 
</p>

osTicket Installation Files Folder -> Double click -> Yes
 <p> 
</p>

![image](https://github.com/user-attachments/assets/bb95ae4b-b8a7-4a3c-a9b9-187a6b7185a0)
 <p> 
</p>

![image](https://github.com/user-attachments/assets/492d0324-89ec-4a2d-9865-8f2958cfa159)
 <p> 
</p>

13. Indstall MySQL5.5.62
 <p> 
</p>

osTicket Installation Files Folder -> Double click -> I agree -> Typical -> Install -> Check Launch -> Finish
 <p> 
</p>

![image](https://github.com/user-attachments/assets/3741db6d-85c4-40d0-93cf-74d7f9015a86)
 <p> 
</p>

![image](https://github.com/user-attachments/assets/2a09d0e1-8342-4ad6-927b-59e3260d3dba)
 <p> 
</p>

![image](https://github.com/user-attachments/assets/f5db121f-645a-47bc-82ef-c8894d184dde)
 <p> 
</p>

![image](https://github.com/user-attachments/assets/dcbe9b1c-8057-4af9-bd3d-7352b313a38a)
 <p> 
</p>

After Application Launched
 <p> 
</p>

Next -> Standard -> Next -> Under "Modify security Settings" type Unername/Password -> *Save to Notepad* -> Next -> Execute -> Finish
 <p> 
</p>

![image](https://github.com/user-attachments/assets/d41bd5fa-9b2c-4bfc-85a9-3861f41277a1)
 <p> 
</p>

![image](https://github.com/user-attachments/assets/e9c0699a-8378-4227-a867-a7a78a067bf1)
 <p> 
</p>

13. Open IIS as Administrator
 <p> 
</p>

In search bar type "IIS", Rt click "IIS" -> Run as administrator
 <p> 
</p>

![image](https://github.com/user-attachments/assets/ed3f8252-1d54-4ad5-b883-1c40310a4191)
 <p> 
</p>

14. Register PHP in IIS
 <p> 
</p>

Open PhP Manager -> Click "Register New PHP Version" -> Browse PHP folder in C drive -> double click "php.cgi" -> OK
 <p> 
</p>

![image](https://github.com/user-attachments/assets/e5a653db-2afc-4c9c-a00c-7139fc8dd63e)
 <p> 
</p>

![image](https://github.com/user-attachments/assets/503b79e0-dc67-4185-89ed-c82a025b5aec)
 <p> 
</p>

![image](https://github.com/user-attachments/assets/1a39de9e-0528-4350-afe8-5375451c7cb2)
 <p> 
</p>

![image](https://github.com/user-attachments/assets/d82c7071-0edb-4693-8976-b1d846694213)
 <p> 
</p>

15. Reload IIS / Stop and Restart the server
 <p> 
</p>

Rt click "osTicket-vm" -> Stop -> Wait a few seconds -> Rt click "osTicket-vm" -> Start
 <p> 
</p>

![image](https://github.com/user-attachments/assets/ebfd0dc7-6152-471e-b738-4ce2e6073b29)
 <p> 
</p>

![image](https://github.com/user-attachments/assets/c78123b8-ff85-47bc-a97a-4575f7c39f1a)
 <p> 
</p>

16. Install osTicket Application
 <p> 
</p>

osTicket Installation Files Folder -> osTicket v1.15.8 -> Rt click -> Extract ->
 <p> 
</p>

![image](https://github.com/user-attachments/assets/417d6940-7d61-4f5c-88b7-41d48d3ba9fd)
 <p> 
</p>

![image](https://github.com/user-attachments/assets/e66b622c-aeaf-4b80-b00f-af1285f64473)
 <p> 
</p>

17. Open ->  copy "Upload" folder -> browse to "c:\inetphp\wwroot" -> Paste -> Rename "osTicket" spelled extactly
 <p> 
</p>

![image](https://github.com/user-attachments/assets/237610cf-4bb4-4f42-a86d-6a55cb941467)
 <p> 
</p>

![image](https://github.com/user-attachments/assets/4194cb17-48f4-49fa-a53c-8d0cde021e94)
 <p> 
</p>

18. Reload IIS / Stop and Restart the server
 <p> 
</p>

Rt click "osTicket-vm" -> Stop -> Wait a few seconds -> Rt click "osTicket-vm" -> Start
 <p> 
</p>

![image](https://github.com/user-attachments/assets/ebfd0dc7-6152-471e-b738-4ce2e6073b29)
 <p> 
</p>

![image](https://github.com/user-attachments/assets/c78123b8-ff85-47bc-a97a-4575f7c39f1a)
 <p> 
</p>

20. Browse to osTicket
 <p> 
</p>

"osTicket-vm" -> Sites -> Default Web Site -> osTicket -> Browse *80 -> The osTicket website should load
 <p> 
</p>

![image](https://github.com/user-attachments/assets/989c6a9d-a4b0-4628-b6a5-7c322d67575b)
 <p> 
</p>

![image](https://github.com/user-attachments/assets/99c7b951-7fa8-47e4-85ed-e07744a5a3f1)
 <p> 
</p>

21. Enable some features that are not orginally enabled at installation
 <p> 
</p>

In IIS -> Default website -> osTicket -> double click PHP manager -> Enable or disable eextensions -> "php_imap.dll, php_inti.dll, php_opcache.dll, Switch to enable -> Refresh osTicket browser
 <p> 
</p>

![image](https://github.com/user-attachments/assets/141c1f0e-3c77-4d41-906e-c3e577ba6dce)
 <p> 
</p>

![image](https://github.com/user-attachments/assets/c9b9f1d4-9c28-4017-b3f6-5df81ce68397)
 <p> 
</p>

![image](https://github.com/user-attachments/assets/183f3891-a20d-4322-b7d6-3a2693702677)
 <p> 
</p>

22. Rename "c:\intetpub\wwwroot\osTicket\include\ostsampleconfig.php" to "c:\intetpub\wwwroot\osTicket\include\ost-config.php"
 <p> 
</p>

File Explore -> C drive -> inetpub -> wwwroot -> osTicket -> include -> ostsampleconfig.php -> Rt click -> Rename
 <p> 
</p>

![image](https://github.com/user-attachments/assets/58fe374a-6773-4d73-a9f6-f2180091114e)
 <p> 
</p>

![image](https://github.com/user-attachments/assets/71d93031-58c6-49cc-a025-61ceaa140523)
 <p> 
</p>

23. Assgin permission to "ost-config.php"
 <p> 
</p>

Rt click ost-config.php -> Properties -> Security -> Advanced -> Disable Inheritance -> Remave All -> Add -> Under "Enter the object name..." type "everyone" -> Check names -> Ok -> Full control -> Apply -> Ok
 <p> 
</p>

![image](https://github.com/user-attachments/assets/da1640d1-e8e5-4ad0-889b-ffaac0aea470)
 <p> 
</p>

![image](https://github.com/user-attachments/assets/05cee5b5-49f4-42bf-8f04-8545bca8c11f)
 <p> 
</p>

![image](https://github.com/user-attachments/assets/ecdcf1c9-33e1-4385-b988-4b07f48da13a)
 <p> 
</p>

![image](https://github.com/user-attachments/assets/c9b9a70f-3796-4860-8cf8-bce39620a444)
 <p> 
</p>

![image](https://github.com/user-attachments/assets/4ed1c165-587a-4baf-a788-a1e25657fdf7)
 <p> 
</p>

![image](https://github.com/user-attachments/assets/4db623b6-175f-4ba3-8c68-a3bb4eef91ed)
 <p> 
</p>

24. Finsih setting up osTicket
 <p> 
</p>

osTicket browser -> Continue -> Enter Help Desk Name -> Enter email address -> Enter admin user -> Enter admin email (differnt from previouly entered email) -> Enter Username/password -> Save credintials to notepad
 <p> 
</p>

![image](https://github.com/user-attachments/assets/5b50902d-9034-4a1b-a6d2-5571eef35f67)
 <p> 
</p>

25. Install Heidi SQL *Create a database specifically for osTicket*
 <p> 
</p>

osTicket Installation Files Folder -> Heidi SQL -> I accept... -> Next four times -> Install -> *Make sure Launch is checked* -> Finish ->
 <p> 
</p>

![image](https://github.com/user-attachments/assets/57f36afc-4fd4-4f51-aedd-7fa72a352202)
 <p> 
</p>

![image](https://github.com/user-attachments/assets/9c86b182-e29c-4af2-a9e7-97d8682c86ad)
 <p> 
</p>

After Application Launched
 <p> 
</p>

Skip -> New  -> Enter User/Password (same as setting up MySQL) -> Open/Connect to Database -> Rt "Unnamed" -> Create New -> Database -> Type "osTicket" spelled extactly in "Name" -> Ok
 <p> 
</p>

![image](https://github.com/user-attachments/assets/eefda6e7-3e27-4d41-bfae-c48c83cc633b)
 <p> 
</p>

![image](https://github.com/user-attachments/assets/0c652fe1-4848-4448-bd6a-88e6fa707831)
 <p> 
</p>

![image](https://github.com/user-attachments/assets/a7006b52-8698-4ec5-8c4b-b93ed3128a92)
 <p> 
</p>

![image](https://github.com/user-attachments/assets/67d4b267-fa9c-434d-a90c-17185d378fa9)
 <p> 
</p>

![image](https://github.com/user-attachments/assets/c4e2927b-767f-4f48-bf5d-afbb479b6e34)
 <p> 
</p>

![image](https://github.com/user-attachments/assets/757b72a6-4989-4daf-869c-34d9df44b2cc)
 <p> 
</p>

26. Finsih setting up osTicket "Database settings"
 <p> 
</p>

osTicket browser ->  Under "MySQL Database" type "osTicket" (database created in previous step) ->  Under "MySQL Username" enter username (same as setting up MySQL) ->  Under "MySQL Password" enter password (same as setting up MySQL) -> Install Now
 <p> 
</p>

![image](https://github.com/user-attachments/assets/912314f6-5dd0-47b5-b915-38e9a0689100)
 <p> 
</p>

![image](https://github.com/user-attachments/assets/03d4f357-a8e3-407d-8d17-8e5c8ec043a5)
 <p> 
</p>

Congratulations. If you followed these steps exactly you have successfully installed the free ticketing software osTicket. Now you can continue to the next lab for practice creating and solving simulated real world Help desK tickets.
