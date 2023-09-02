# osticket-prereqs
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
First create an account for Microsoft Azure 

*Step 1 Create a Resource group and Virtual Machine in Microsoft Azure.
![Create A Resource Group](https://github.com/Ken7281/osticket-prereqs/assets/142465932/0adb9691-2d45-4994-9156-8f7378adcabe)
*When creating the Virtual Machine make sure to select the Resource Group you created.*

![Creating A Virtual Machine 1](https://github.com/Ken7281/osticket-prereqs/assets/142465932/19fd9d15-68f8-41c2-be23-a1a7d45692f4)
*Name the Virtual Machine. Select Windows 10 as the image, and create a username and password  for the Virtual Machine.*

![Creating A Virtual Machine 2](https://github.com/Ken7281/osticket-prereqs/assets/142465932/7ce60b0d-79da-4ec8-afe0-88a23d2d7906)
*Agree to the terms and conditions and select review + create*

*After creating the Virtual Machine, use Remote Desktop ino the Virtual Machine using it's IP adress*
On the Virtual Machine search for Internet Information Services Manager (IIS) 
Select "turn windows features on or off", then select "internet information services". Select the "world wide web services" box, select "application Development Features", check the CGI Box. 
Go to "Common HTTP features" and check all of the boxes and click ok to confirm the changes. 
![Turning Off Some Windows Features](https://github.com/Ken7281/osticket-prereqs/assets/142465932/5baca146-aa87-438a-9a1c-c850b11d8e63)

*Download "PHP Manager*

On the windows file explorer go to Windows C and creat a new folder. Install PHP 7.3.8 and extract all files into the PHP folder. 

*Download VC_redist.x86.exe* 

*Download & install mysql-5.5.62-win32.msi* The username is root, create a password and complete the download. 

On the start menu select IIS ticket and right click to run as an administrator.
![Running IIS as an administrator](https://github.com/Ken7281/osticket-prereqs/assets/142465932/31d56c6c-f872-4793-8f36-f39ab6d9383e)
Select PHP Manager, click register new PHP version, click on the dash on the right to the C: drive and open the PHP folder. Click PHP-CGI and press ok. Select the virtual machine you created and restart.




- Item 5

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
