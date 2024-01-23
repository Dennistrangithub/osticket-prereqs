
<p align="center">
    <img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>
<h1>osTicket - Prerequisites and Installation</h1>
<p>
    Hello, my name is Dennis, and I am an IT professional with expertise in systems administration and cloud solutions. This documentation outlines my work on deploying the open-source help desk ticketing system osTicket on a Windows 10 Azure Virtual Machine. This project highlights my skills in cloud computing, system setup, and problem-solving.
</p>

<h2>Project Overview</h2>
<p>
    This project aimed to implement osTicket, a customer support ticket system, in a cloud environment. Key challenges included configuring the system for optimal performance and security on Azure and ensuring a seamless installation process. My role involved not only the technical implementation but also optimizing the environment for reliability and scalability.
</p>

<h2>Environments and Technologies Used</h2>
<ul>
    <li>Microsoft Azure (Virtual Machines/Compute)</li>
    <li>Remote Desktop</li>
    <li>Internet Information Services (IIS)</li>
</ul>

<h2>Operating Systems Used</h2>
<ul>
    <li>Windows 10 (21H2)</li>
</ul>

<h2>List of Prerequisites</h2>
<ul>
    <li>Microsoft Azure subscription</li>
    <li>Windows 10 Virtual Machine (VM)</li>
    <li>Internet Information Services (IIS)</li>
    <!-- Add other prerequisites as needed -->
</ul>

<h2>Installation Steps</h2>
<h3>Step 1: Setting up Azure/VM machines</h3>
I initiated the project by installing a Windows 10 Virtual Machine in Microsoft Azure. This involved:
<ul>
    <li>Creating a new Resource Group in Azure for organized management.</li>
    <li>Configuring a Windows 10 VM with 2-4 Virtual CPUs, ensuring the creation of a new Virtual Network for secure and scalable networking.</li>

</ul>
<img src="https://github.com/Dennistrangithub/osticket-prereqs/assets/152820266/6b69bbfc-e2f3-4239-9c4e-ca9d39a3fd4c" height="80%" width="80%" alt="Disk Sanitization Steps"/>


</p>

<p>
<h3>Step 2: Downloading Files for Installation/Configuring IIS</h3>
The next step was preparing the VM for osTicket installation, which included:
<ul>
    <li>Installation and configuration of Internet Information Services (IIS) for hosting the ticketing system.</li>
    <li>Ensuring all necessary security features and updates were applied to the VM for a secure operating environment.</li>
    <li>Downloaded any files necessary for installation</li>
    <!-- Add other system preparation steps here -->
</ul>

1. **Install and Configure Internet Information Services (IIS)**:
    
    - On your VM, access the Control Panel.
    - Navigate to "Programs" and then "Turn Windows features on or off".
    - Check the boxes for "World Wide Web Services", "Application Development Features", and "IIS Management Console".
    - Ensure CGI and Common HTTP Features are enabled.
    <img src="https://github.com/Dennistrangithub/osticket-prereqs/assets/152820266/d19d7ce4-6925-4593-afc6-572fbccfbcad" alt="IIS Setup"/>
   Checking boxes for CGI and Common HTTP Features
    <img src="https://github.com/Dennistrangithub/osticket-prereqs/assets/152820266/761f1a3a-b33f-4694-b4a1-c9a84079f8b2" alt="IIS Setup"/>
   Checking boxes for IIS Management Console
    <img src="https://github.com/Dennistrangithub/osticket-prereqs/assets/152820266/440b7198-0f55-4f4b-a01c-16f403705702" alt="IIS Setup"/>
    For this, we check if IIS is enabled through this address (127.0.0.1)
    

2. **Download Necessary Installation Files**:
    
    - Access the provided link for osTicket Installation Files.
    - Download required files such as PHP Manager for IIS, Rewrite Module, PHP 7.3.8, VC_redist.x86.exe, and MySQL 5.5.62.
      
<img src="https://github.com/Dennistrangithub/osticket-prereqs/assets/152820266/266836eb-93d2-4881-96a4-da1e755c41ba" alt="IIS Setup"/>
<img src="https://github.com/Dennistrangithub/osticket-prereqs/assets/152820266/c1986d58-b6be-4592-90e4-92316bd9ac68" alt="IIS Setup"/>
</p>

<p>
<h3>Step 3: Installing osTicket</h3>

1. **Install osTicket**:
    
    - Unzip and install downloaded files in the appropriate directories (e.g., PHP files in C:\PHP).
    - Open IIS as an Admin and register PHP.
    - Install osTicket v1.15.8 by extracting the "upload" folder to c:\inetpub\wwwroot and renaming it to "osTicket".
    - Enable necessary PHP extensions like php_imap.dll, php_intl.dll, and php_opcache.dll through the PHP Manager in IIS.
    - Assign appropriate permissions to the ost-config.php file.
      

https://github.com/Dennistrangithub/osticket-prereqs/assets/152820266/3ef16412-dc34-4729-9f8e-c193dacf483b


<img src="https://github.com/Dennistrangithub/osticket-prereqs/assets/152820266/82fe575d-fdfa-47e5-8670-b77428b5ce0e"/>
Installed PHP Manager for IIS
<img src="https://github.com/Dennistrangithub/osticket-prereqs/assets/152820266/01aad24d-b494-41a9-add0-099bd1bd916b"/>
Installed Rewrite Module
<img src="https://github.com/Dennistrangithub/osticket-prereqs/assets/152820266/6ae4af03-4f3b-4442-964c-a6fa88278369"/>
</p>
For this to happen we make a new folder within the main drive called "PHP", then we extract the folder contents for PHP into that folder
<img src="https://github.com/Dennistrangithub/osticket-prereqs/assets/152820266/57678c5a-9078-42fb-9ad4-860587c47396"/>
We install the VC_redist.x86.exe
<img src="https://github.com/Dennistrangithub/osticket-prereqs/assets/152820266/3ef16412-dc34-4729-9f8e-c193dacf483b"/>
</p> 
For this, we set up MySQL


 ## 1a. Changing PHPs:
    
<li>Open IIS as an Admin and register PHP.
<li>Install osTicket v1.15.8 by extracting the "upload" folder to c:\inetpub\wwwroot and renaming it to "osTicket".
<li>Enable necessary PHP extensions like php_imap.dll, php_intl.dll, and php_opcache.dll through the PHP Manager in IIS.
<li>Assign appropriate permissions to the ost-config.php file.
<img src="https://github.com/Dennistrangithub/osticket-prereqs/assets/152820266/1738be84-928c-420d-ab47-a72f7de45476"/>
<img src=""/>
<img src=""/>
<img src=""/>
<img src=""/>


2. **Set Up osTicket Database**:
    
    - Install HeidiSQL and create a new database session for osTicket.
    - Create a database named "osTicket" using the HeidiSQL interface.
    - Continue setting up osTicket in the browser by configuring the database with the created MySQL database details.
<img src=""/>
<img src=""/>
<img src=""/>
<img src=""/>
<img src=""/>

3. **Finalize Installation and Configuration**:
    
    - Once the osTicket installation is complete, access the help desk login page to ensure it's working.
    - Perform clean-up tasks like deleting the setup folder and setting read-only permissions for the ost-config.php file.
    - Configure roles, departments, teams, users, SLA, and help topics in the osTicket admin panel.
<img src=""/>
<img src=""/>
<img src=""/>
<img src=""/>
<img src=""/>
<ul>
    
</ul>
<img src="https://github.com/Dennistrangithub/osticket-prereqs/assets/152820266/0e82d5fc-a26b-42fc-869c-77f37477a4ce"/>

<img src="https://github.com/Dennistrangithub/osticket-prereqs/assets/152820266/ce8f6c5f-77da-46cc-a9bb-411c7b8c00df"/>

<img src="https://github.com/Dennistrangithub/osticket-prereqs/assets/152820266/0280d6eb-7dc1-4a44-9c8e-917754bc95d9"/>
</p>

<p>
    <h2>Conclusion</h2>
    This project was a significant learning opportunity for me, allowing me to deepen my understanding of cloud environments and system administration. It also helped me develop my problem-solving skills, particularly in configuring and optimizing software in a cloud-based setting.
</p>

</body>
</html>
