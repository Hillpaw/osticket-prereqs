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

- Windows 10</b> (22H2)

<h2>List of Prerequisites</h2>

- Install and Enable IIS (Internet Information Services) in Windows with CGI and common HTTP Features
- Install [PHP Manager for IIS](https://drive.google.com/file/d/1RHsNd4eWIOwaNpj3JW4vzzmzNUH86wY_/view?usp=share_link)
- Install [Rewrite Module](https://drive.google.com/file/d/1tIK9GZBKj1JyUP87eewxgdNqn9pZmVmY/view?usp=share_link)
- Create a directory on the PC (ex. C:\PHP)
- Install [PHP 7.3.8](https://drive.google.com/file/d/1snNMtLdCOpMtkCyD4mvl9yOOmvVIp9fP/view?usp=share_link)
- Install [VC_redist.x86.exe](https://drive.google.com/file/d/1s1OsGF3-ioO0_9LYizPRiVuIkb3lFJgH/view?usp=share_link)
- Install [MySQL 5.5.62](https://drive.google.com/file/d/1_OWh9p7VQLcrB0q_V7qT8yHl0xo5gv7z/view?usp=share_link)

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/WMFM4hk.png" alt="Windows Features"/>
</p>
<p>
Search in Windows: "Windows Features on and off" -> 
Search for Internet Information Services -> World Wide Web Services -> Application Development Features ->
Make sure to check [X] CGI here.
Now look for [X] Common HTTP Features (also under World Wide Web Services)
Make sure everything is checked in here. 

If you do not see anything, other than an error, make sure to go back to the Windows Features window again and uncheck Internet Information Services until it is uninstalled, and then check the box again to reinstall. 
</p>
<br />

<p>
<img src="[https://i.imgur.com/WMFM4hk.png](https://i.imgur.com/tHnpZ98.png)" alt="osTicket extensions"/>
</p>
<p>
Note that some extensions are not enabled. Go back to IIS, then go to Sites -> Default -> osTicket and double-click PHP Manager.
Click "Enable or Disable an extention" and enable the following extensions:
1. Enable: php_imap.dll
2. Enable: php_intl.dll
3. Enable: php_opcache.dll
After that is done, refresh the osTicket site in your browser, and observe the changes.
</p>
<br />

<p>
<img src="[https://i.imgur.com/WMFM4hk.png](https://i.imgur.com/4xWwEGN.png)" alt="ReadExecute and Read Only"/>
</p>
<p>
Set the permissions on c:\inetpub\wwwroot\osTicket\include\ost-config.php file to Read & Execute and Read only.
</p>
<br />

<p>
<img src="[https://i.imgur.com/WMFM4hk.png](https://i.imgur.com/b8t8CPd.png)" alt="osTicket Control Panel"/>
</p>
<p>
After everything is set, you will be greeted by the Staff Control Panel screen
</p>
<br />
