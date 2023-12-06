<!DOCTYPE html>
<html>
<head>
<h1>osTicket - Prerequisites and Installation</h1>
</head>
<body>

<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<p>
    Hello, my name is Dennis, and I am an IT professional with expertise in systems administration and cloud solutions. This documentation outlines my work on deploying the open-source help desk ticketing system osTicket on a Windows 10 Azure Virtual Machine. This project highlights my skills in cloud computing, system setup, and problem-solving.
</p>

<h2>Project Overview</h2>
<p>
    The aim of this project was to implement osTicket, a customer support ticket system, in a cloud environment. Key challenges included configuring the system for optimal performance and security on Azure and ensuring a seamless installation process. My role involved not only the technical implementation but also optimizing the environment for reliability and scalability.
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
<strong>Step 1: Creating the Virtual Environment</strong><br />
I initiated the project by setting up a Windows 10 Virtual Machine in Microsoft Azure. This involved:
<ul>
    <li>Creating a new Resource Group in Azure for organized management.</li>
    <li>Configuring a Windows 10 VM with 2-4 Virtual CPUs, ensuring the creation of a new Virtual Network for secure and scalable networking.</li>
</ul>
<img src="https://github.com/Dennistrangithub/osticket-prereqs/assets/152820266/6b69bbfc-e2f3-4239-9c4e-ca9d39a3fd4c" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
<strong>Step 2: Preparing the System</strong><br />
The next step was preparing the VM for osTicket installation, which included:
<ul>
    <li>Installation and configuration of Internet Information Services (IIS) for hosting the ticketing system.</li>
    <li>Ensuring all necessary security features and updates were applied to the VM for a secure operating environment.</li>
    <!-- Add other system preparation steps here -->
</ul>
<img src="https://github.com/Dennistrangithub/osticket-prereqs/assets/152820266/266836eb-93d2-4881-96a4-da1e755c41ba" alt="IIS Setup"/>
<img src="https://github.com/Dennistrangithub/osticket-prereqs/assets/152820266/440b7198-0f55-4f4b-a01c-16f403705702" alt="IIS Setup"/>
</p>

<p>
<strong>Step 3: Installing osTicket</strong><br />
Finally, I installed and configured osTicket on the VM:
<ul>
    <li>Downloading the osTicket installation files from the official source.</li>
    <li>Following the installation wizard, I customized settings to fit our organizational needs, focusing on user accessibility and security.</li>
    <!-- Detail any specific settings or configurations needed -->
</ul>
<img src="https://github.com/Dennistrangithub/osticket-prereqs/assets/152820266/0e82d5fc-a26b-42fc-869c-77f37477a4ce"/>

<img src="https://github.com/Dennistrangithub/osticket-prereqs/assets/152820266/ce8f6c5f-77da-46cc-a9bb-411c7b8c00df"/>

<img src="https://github.com/Dennistrangithub/osticket-prereqs/assets/152820266/0280d6eb-7dc1-4a44-9c8e-917754bc95d9"/>
</p>


</body>
</html>
