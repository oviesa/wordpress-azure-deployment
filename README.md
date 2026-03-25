WordPress Deployment on Azure VM
Overview

This project demonstrates the deployment of a WordPress website on a Microsoft Azure Ubuntu virtual machine using Apache, MariaDB, and PHP. The goal was to simulate a real-world Linux web server deployment and gain experience with cloud infrastructure and system configuration.

Technologies Used
Microsoft Azure
Ubuntu Linux
Apache2
MariaDB
PHP
WordPress
Linux CLI
Features
Linux server configuration
Apache web server setup
Database integration with MariaDB
WordPress installation and configuration
Security plugin implementation
Responsive theme customization
Architecture

Basic deployment architecture:

User → Azure VM → Apache → PHP → MariaDB → WordPress

(Add architecture diagram here if)

Installation Steps
1 Create Azure VM
Created Ubuntu virtual machine
Configured networking and firewall rules
Connected via SSH
2 Install Apache
sudo apt update
sudo apt install apache2
3 Install MariaDB
sudo apt install mariadb-server
4 Install PHP
sudo apt install php php-mysql
5 Install WordPress
Downloaded WordPress
Configured wp-config.php
Set file permissions
6 Configure Security
Installed WordPress security plugins
Configured firewall rules
Screenshots

(Add screenshots here)

Challenges Faced
Resolving Linux permission issues
Configuring Apache virtual hosts
Debugging database connection errors
Lessons Learned
Linux server administration
Cloud VM management
LAMP stack configuration
WordPress production deployment workflow
Future Improvements
Docker container deployment
Automated deployment scripts
CI/CD integration
Monitoring setup
