Assignment 7: Host a Web Application Stack on Ubuntu Linux
This repository contains the work for implementing a LAMP (Linux, Apache, MySQL, PHP) stack on an Ubuntu 24.04 Virtual Machine. This environment replicates the production stack for a Human Resources Employee Database application, enabling consistent local development and testing.

Overview
The purpose of this project was to set up a fully functional LAMP stack development environment for the HR Employee Database application. Key tasks included installing and configuring Apache, MariaDB, and PHP, as well as deploying a sample database with 300,000 records.

Features
VM Configuration:
Ubuntu 24.04 with 2 vCPUs, 2GB RAM, and 25GB storage.
Dual network adapters: NAT for internet and Host-Only for local access.
Apache Web Server:
Hosted static and dynamic web content.
MariaDB (MySQL):
Installed and secured for database management.
Loaded with a sample HR database for testing.
PHP Integration:
Configured to enable server-side scripting and database interaction.
Custom Web Pages:
Designed and deployed an HTML home page and PHP scripts to verify functionality.
Repository Structure
docs/: Documentation for LAMP stack configuration and deployment.
www/: Web content and scripts hosted on the server:
index.html: Custom static home page.
phptest.php: PHP script for verifying PHP functionality.
helloworld.php: PHP script displaying "Hello World!".
sql/: SQL scripts for querying and managing the HR database.
Setup and Configuration
1. Virtual Machine Setup
Configured an Ubuntu 24.04 Virtual Machine with:
2 vCPUs, 2GB RAM, 25GB storage.
Networking: NAT and Host-Only adapters.
2. Apache Installation
Installed Apache2 to serve web content.
Verified the default web page using the server's IP address.
3. PHP Installation
Installed PHP and required modules.
Created phptest.php to verify PHP functionality:
php
   
<?php
phpinfo();
?>
4. MariaDB Installation
Installed MariaDB and secured the database server.
Created a database user for secure access:
sql
   
CREATE USER 'devuser'@'localhost' IDENTIFIED BY 'password';
GRANT ALL PRIVILEGES ON *.* TO 'devuser'@'localhost';
FLUSH PRIVILEGES;
5. Loading Sample Data
Cloned the HR database repository:

   
git clone https://github.com/datacharmer/test_db.git
Imported the database into MariaDB:
css
   
mysql -u devuser -p < employees.sql
6. Testing and Verification
Queried the database to confirm data loading:
sql
   
SELECT COUNT(*) FROM employees;
Created dynamic web pages such as helloworld.php to test PHP and database integration.
How to Use
Clone the repository:

   
git clone https://github.com/your-username/assignment7-lamp-stack
Follow the setup guide in docs/setup.md for configuring the LAMP stack.
Copy the contents of the www/ folder to /var/www/html on your server.
Access the application through the browser using the server’s IP address.
Technologies Used
Linux: Operating System for the VM.
Apache: Web server for hosting applications.
MariaDB: Database server for managing data.
PHP: Server-side scripting language.
VirtualBox: Virtualization platform for creating the VM.
