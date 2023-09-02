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
Files used
![Files Used For OsTicket](https://github.com/Ken7281/osticket-prereqs/assets/142465932/4f7a33ef-e110-459b-8170-c975a20e3d98)

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

*Download "PHPManagerForIIS_V1.5.0.msi*

On the windows file explorer go to Windows C and creat a new folder. Install PHP 7.3.8 and extract all files into the PHP folder. 

*Download VC_redist.x86.exe* 

*Download & install mysql-5.5.62-win32.msi* The username is root, create a password and complete the download. 

On the start menu select IIS ticket and right click to run as an administrator.
![Running IIS as an administrator](https://github.com/Ken7281/osticket-prereqs/assets/142465932/31d56c6c-f872-4793-8f36-f39ab6d9383e)
Select PHP Manager, click register new PHP version, click on the dash on the right to the C: drive and open the PHP folder. Click PHP-CGI and press ok. Select the virtual machine you created and restart.

*Download osTicket-v1.15.8.zip* double click to open the zipped file. Open the windows C: and open inetpub and open the wwwroot folder.
On a seperate file manger drag the upload folder from the osticket zippped file into the wwwroot folder. Rename the upload folder to OsTicket. 
![Moving the Upload Folder To The wwroot folder on the C; drive](https://github.com/Ken7281/osticket-prereqs/assets/142465932/47e21d26-2fa8-4479-ba23-1447573057f4)

<p>
</p>
<p>
Restart the virtual machine as an administrator. Under the virtual machines connections tab 
expand sites, expand default web site, and double click OsTicket. On the right click browse *80 and open OsTicket installer.
  
 ![Browsing To The osTicket site](https://github.com/Ken7281/osticket-prereqs/assets/142465932/9e11855e-a4d6-48d1-9361-a410ec48027d)

<p>
Double click PHP Manager and selecet disable an extension
  enable PHP imap.dll, enable PHP intl.dll, enable PHP opcache.dll, and refresh the OsTicket web page. Go to the OsTicket folder in the wwwroot folder. open the include folder and rename the ost-sampleconfig.php to ost-config.php.
right click ost-config and select properties, select security, select advanced and disable inheritance. Remove all of the inherited permissions and click add.
select "principal and type "everyone" into the objects name box and click check names and click ok. Under basic permissions select the full control box and click apply and ok to confirm the changes. 
</p>
<p>
Click continue on the OsTicket installer and create a "name" and "email" and complete the admin user information. 
  
 ![HelpDesk Setup](https://github.com/Ken7281/osticket-prereqs/assets/142465932/dd2f71cb-ed9b-4fe4-bf5a-cb20c9f9319d)
</p>
<br />
*Download HeidiSQL_12.3.0.6589_Setup.exe* 
Open HeidiSQL and ricght click on unnamed. Click create new, and select database. Name the database OsTicket & click ok. 

![Creating a new database in Heidisql](https://github.com/Ken7281/osticket-prereqs/assets/142465932/6901f8ec-9a58-4aef-9f31-96ffda845cfd)
<p>
Type OsTicket on the MySQL database. Under database settings click install OsTicket.
</p>
<p>
Go to the inetpub folder in the files manager, select wwwroot, selest OsTicket and delete the setup folder. 
Double click the include folder under OsTicket right click ost-config and select properties, select security, select advanced. Click on everyone and click edit. Uncheck full control, modify, and write and click apply and ok. 
</p>
<br />
OsTicket should be fully operational, and you should be able to login with the information you previously created.
