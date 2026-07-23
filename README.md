# osTicket Prerequisites and Installation

## 📋 Project Overview

This project demonstrates the installation and configuration of the osTicket Help Desk Ticketing System on a Windows 10 Azure Virtual Machine.

## 🎯 Objectives

- Deploy a Windows 10 Virtual Machine in Microsoft Azure
- Install Internet Information Services (IIS)
- Install PHP and MySQL
- Configure IIS for osTicket
- Install the osTicket application
- Verify successful installation by logging into the Admin Panel

## 🛠️ Technologies Used

- Microsoft Azure
- Windows 10
- IIS (Internet Information Services)
- PHP
- MySQL
- osTicket

### Step 1 - Create an Azure Windows 10 Virtual Machine
<img width="1357" height="613" alt="Screenshot 2026-07-22 200002" src="https://github.com/user-attachments/assets/56d31b6c-3ddd-400d-80a8-15b002c286f3" />
This project begins by creating a Windows 10 virtual machine inside Microsoft Azure
<img width="1215" height="481" alt="Screenshot 2026-07-22 200942" src="https://github.com/user-attachments/assets/12fe3464-cc31-4ea3-866f-ad2366eaae83" />
<img width="452" height="247" alt="Screenshot 2026-07-22 201138" src="https://github.com/user-attachments/assets/cb0360d4-094b-480b-a8cf-6cfb991c583d" />
After i created the VM, the public IP address will be used to login into the vm using Remote Desktop Connection.
 Step 2 -Download OsTicket installation files
<img width="1109" height="474" alt="hhh" src="https://github.com/user-attachments/assets/1cb8d2b5-8316-4658-b922-ff22e98f7da2" />
After signinng into Windows 10 virtual machine,the installation package contanining all required osTicket files was extracted.The download links for each file included in the installation package.
 Step 3 -Enable IIS in Windows with CGI
 Internet Information Service is Mirsosoft's built-in web server for windows.it enabled to host the osTicket website.During installation,the CGI(Common Gateway Interface) feature was also enabled because osTicket is built with PHP.CGI allowsIIS to process PHP scripts and display the web application correctly.
<img width="519" height="536" alt="ppp" src="https://github.com/user-attachments/assets/d48b14c6-23a1-4940-aff8-a82a26c55818" />
Process beings by typing "Control pannel" in the serach nextto the Windows icon.Then uninstall a program.after that click Turn Windowns features on or off
<img width="495" height="434" alt="kkk" src="https://github.com/user-attachments/assets/b89213dc-21b0-48c9-b73c-75e61b474f4e" />
Inside Windows Features the first step is to check the box next "Internet Information Sercices" to turn IIS on.
<img width="418" height="374" alt="Annotation 2026-07-23 014007" src="https://github.com/user-attachments/assets/02f29a1d-f8a6-4865-bd25-b4cbd8615301" />
Now click + sign next to "internet information Services" to expand the folder.Then expand the "World Wide Web Services"folder and expand "Application Development Features" folder.Check the box next to "CGI.Then click "OK" to install IIS with CGI installation.
<img width="648" height="459" alt="Annotation 2026-07-23 014133" src="https://github.com/user-attachments/assets/07f6f9c0-a0d1-4552-8971-274f6721b4fd" />
Now IIS and 
 Step 4 - Install PhP Manager for IIS
<img width="486" height="392" alt="Annotation 2026-07-23 015906" src="https://github.com/user-attachments/assets/688ee305-4ad0-4720-9a60-ba0b6987ef6a" />
PHP Manager for IIS has been successfully installed
 Step 5 - Install Rewrite Module 
<img width="496" height="382" alt="ppppp" src="https://github.com/user-attachments/assets/7ebffaf2-f7d5-4f19-abca-2b02f6d2bb9b" />
The rewrite Module has been installed
Step 6 -Place PHP files into the "C:PHP" folder
<img width="836" height="498" alt="AAA" src="https://github.com/user-attachments/assets/14ecb14d-bef2-495d-bbb9-25f87a720d84" />
The first step in this next installation will be to create a new folding on the C:\ drive called "PHP".
<img width="613" height="378" alt=",,,,,&#39;" src="https://github.com/user-attachments/assets/cd8929e4-64ab-4b3c-8d26-5ef754f9c79e" />
Since the PHP files were downloaded in a ZIP folder, I extracted them to C:\PHP by right-clicking the file and selecting "Extract All...". This allows IIS to access PHP so osTicket can run properly.
<img width="627" height="442" alt="BBBB" src="https://github.com/user-attachments/assets/47034281-84b3-4d28-ae48-52fefa13ab90" />
The destination for the extraction will be "C:\PHP".
<img width="784" height="605" alt="77777" src="https://github.com/user-attachments/assets/abbac249-fa4c-4247-b489-f76d472552cd" />
After extracting the files to C:\PHP, the PHP installation was organized in one location. This allows IIS to find and use PHP so osTicket can run properly.
Step 7-Install Microsoft Visual Studio C+ Redistributable
<img width="477" height="309" alt="4444" src="https://github.com/user-attachments/assets/e7591e85-dd34-41f4-907c-c7c76fc5bf8f" /> 
Next, I installed the Microsoft Visual C++ Redistributable. This is required because PHP and MySQL depend on it to run on Windows. Without it, osTicket may not function correctly
<img width="490" height="292" alt="000" src="https://github.com/user-attachments/assets/08a13da6-5f8a-45a4-8003-f367a8e37194" />
Installation was successful.
Step 8 -Intal MySQL
<img width="500" height="404" alt="AAAN" src="https://github.com/user-attachments/assets/501555c5-6de4-4610-a701-fab6b1c3607e" />
 Next, I installed MySQL Server, which is the database osTicket uses to store all of its information. This includes tickets, user accounts, and settings. Without MySQL, osTicket wouldn't have a place to save its data, so it wouldn't work properly.
 <img width="491" height="386" alt="TTTT" src="https://github.com/user-attachments/assets/9b8352d1-2701-4f6a-8d50-2de3cf5668df" />
 Once the installation was complete, I checked the box to launch the MySQL Instance Configuration Wizard. The wizard was used to configure the MySQL server and create the settings needed for osTicket to connect to the database successfully. 
 <img width="500" height="404" alt="AAAN" src="https://github.com/user-attachments/assets/e9a94ae6-8544-4381-b1c4-837d002923fe" />
<img width="491" height="381" alt="53" src="https://github.com/user-attachments/assets/175097f8-e4be-4177-b80b-bcf3770df566" />
Select standard configuration.
<img width="494" height="369" alt="uuu" src="https://github.com/user-attachments/assets/91f37653-7bf1-44b9-a247-8a7d812292a9" />
MySQL has been succesful installed.
Step 9 -Register PHP from within IIS
<img width="777" height="446" alt="IISS" src="https://github.com/user-attachments/assets/01bd3b28-b3e4-4819-8f19-b8ab9821a2e8" />
Once the installation was complete, I checked the box to launch the MySQL Instance Configuration Wizard. The wizard was used to configure the MySQL server and create the settings needed for osTicket to connect to the database successfully. 

 
<img width="1086" height="579" alt="1222" src="https://github.com/user-attachments/assets/e080b473-bb0b-438e-9510-116c34f4577d" />

