<p align="center">
    <img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

# osTicket - Prerequisites and Installation :computer:

Hello, my name is Dennis, and I am an IT professional with expertise in systems administration and cloud solutions. This documentation outlines my work on deploying the open-source help desk ticketing system osTicket on a Windows 10 Azure Virtual Machine. This project highlights my skills in cloud computing, system setup, and problem-solving.

## Project Overview :mag:

This project aimed to implement osTicket, a customer support ticket system, in a cloud environment. Key challenges included configuring the system for optimal performance and security on Azure and ensuring a seamless installation process. My role involved not only the technical implementation but also optimizing the environment for reliability and scalability.

## Environments and Technologies Used :gear:

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

## Operating Systems Used :computer:

- Windows 10 (21H2)

## List of Prerequisites :clipboard:

- Microsoft Azure subscription
- Windows 10 Virtual Machine (VM)
- Internet Information Services (IIS)
<!-- Add other prerequisites as needed -->

## Installation Steps :hammer_and_wrench:

### Step 1: Setting up Azure/VM machines

I initiated the project by installing a Windows 10 Virtual Machine in Microsoft Azure. This involved:

- Creating a new Resource Group in Azure for organized management.
- Configuring a Windows 10 VM with 2-4 Virtual CPUs, ensuring the creation of a new Virtual Network for secure and scalable networking.

<img src="https://github.com/Dennistrangithub/osticket-prereqs/assets/152820266/6b69bbfc-e2f3-4239-9c4e-ca9d39a3fd4c" height="80%" width="80%" alt="Azure VM Setup"/>

### Step 2: Downloading Files for Installation/Configuring IIS

The next step was preparing the VM for osTicket installation, which included:

- Installation and configuration of Internet Information Services (IIS) for hosting the ticketing system.
- Ensuring all necessary security features and updates were applied to the VM for a secure operating environment.
- Downloading any files necessary for installation
<!-- Add other system preparation steps here -->

#### 1. Install and Configure Internet Information Services (IIS):

- On your VM, access the Control Panel.
- Navigate to "Programs" and then "Turn Windows features on or off".
- Check the boxes for "World Wide Web Services", "Application Development Features", and "IIS Management Console".
- Ensure CGI and Common HTTP Features are enabled.

<img src="https://github.com/Dennistrangithub/osticket-prereqs/assets/152820266/d19d7ce4-6925-4593-afc6-572fbccfbcad" alt="IIS Setup"/>

#### 2. Download Necessary Installation Files:

- Access the provided link for osTicket Installation Files.
- Download required files such as PHP Manager for IIS, Rewrite Module, PHP 7.3.8, VC_redist.x86.exe, and MySQL 5.5.62.

<img src="https://github.com/Dennistrangithub/osticket-prereqs/assets/152820266/266836eb-93d2-4881-96a4-da1e755c41ba" alt="Downloading Installation Files"/>

### Step 3: Installing osTicket

#### 1. Install osTicket:

- Unzip and install downloaded files in the appropriate directories (e.g., PHP files in C:\PHP).
- Open IIS as an Admin and register PHP.
- Install osTicket v1.15.8 by extracting the "upload" folder to c:\inetpub\wwwroot and renaming it to "osTicket".
- Enable necessary PHP extensions like php_imap.dll, php_intl.dll, and php_opcache.dll through the PHP Manager in IIS.
- Assign appropriate permissions to the ost-config.php file.
<img src="https://github.com/Dennistrangithub/osticket-prereqs/assets/152820266/1738be84-928c-420d-ab47-a72f7de45476" height="50%" width="50%" />
<img src="https://github.com/Dennistrangithub/osticket-prereqs/assets/152820266/fbee1a5c-9fba-404c-9bb9-3b34ec4d1a48" height="70%" width="70%" />
<img src="https://github.com/Dennistrangithub/osticket-prereqs/assets/152820266/b77a30f4-1b0f-44c4-80fc-8aeb691a1432" height="50%" width="50%" />
<img src="https://github.com/Dennistrangithub/osticket-prereqs/assets/152820266/ffa087b5-9550-4d29-b329-c24034a8c72e" height="50%" width="50%" />
<img src="https://github.com/Dennistrangithub/osticket-prereqs/assets/152820266/49490ad4-4167-41b6-aaf3-400ff50d674c" height="50%" width="50%" />


#### 2. Set Up osTicket Database:

- Install HeidiSQL and create a new database session for osTicket.
- Create a database named "osTicket" using the HeidiSQL interface.
- Continue setting up osTicket in the browser by configuring the database with the created MySQL database details.
<img src="https://github.com/Dennistrangithub/osticket-prereqs/assets/152820266/c89a0c33-7cf6-4e78-bbf4-2b1da3ecec92" height="80%" width="80%" />

#### 3. Finalize Installation and Configuration:

- Once the osTicket installation is complete, access the help desk login page to ensure it's working.
<img src="https://github.com/Dennistrangithub/osticket-prereqs/assets/152820266/ce8f6c5f-77da-46cc-a9bb-411c7b8c00df" height="80%" width="80%" />

## Conclusion :checkered_flag:

This project was a significant learning opportunity for me, allowing me to deepen my understanding of cloud environments and system administration. It also helped me develop my problem-solving skills, particularly in configuring and optimizing software in a cloud-based setting.
