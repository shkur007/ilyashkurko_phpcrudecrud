Assignment 7: Host a Web Application Stack on Ubuntu Linux

Description
This assignment focuses on hosting a LAMP (Linux, Apache, MySQL, PHP) stack on an Ubuntu Linux virtual machine. The goal is to configure a development environment for a Human Resources Application, enabling developers to work on the application locally with a consistent setup.

Requirements
Hardware
Computer capable of running VirtualBox or other hypervisor
Ubuntu 24.04 Virtual Machine
Software
VirtualBox or VMware
Ubuntu 24.04 Server OS
Apache2 Web Server
PHP Programming Language
MariaDB (MySQL) Database Server

Key Components

Part 1: Install Apache2 and PHP
Install the Apache2 web server.
Verify Apache is running and accessible via a browser.
Create a custom index.html page.
Install PHP and verify its functionality using a test PHP file.

Part 2: Install MariaDB
Install and secure MariaDB.
Create a new MySQL user and configure access.
Test database functionality by loading a sample dataset (300,000 records from GitHub).

Part 3: Documentation
Document your LAMP stack setup with system specifications and instructions.
Create a block diagram showing the architecture of your setup.

How to Run

Clone the Repository
Ensure all required files are available in your working directory. Clone the repository to access scripts and configuration files.

  
   
git clone <repository-url>
cd <repository-folder>
Setup Apache and PHP
Follow the provided script or manual instructions to install and configure Apache2 and PHP.

Setup MariaDB

Use the commands in the assignment to install, secure, and test MariaDB.

Verify LAMP Stack

Navigate to the server’s IP address in your browser.
Test PHP and database connectivity.

Notes

Ubuntu Setup:
Ensure your VM has at least 2 GB of RAM, 2 vCPUs, and 25 GB of storage.
Networking:
Use both NAT and Host-Only network adapters for connectivity.
Test URLs:
http://<vm-ip-address>
http://<vm-ip-address>/phpinfo.php
Repository Files
index.html: Sample homepage for Apache.
phptest.php: Script to verify PHP installation.
MariaDB configuration files and SQL samples.
