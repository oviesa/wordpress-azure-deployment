# Deployment Process Documentation

## Project Purpose

The goal of this project was to deploy a production-style WordPress application on a cloud-hosted Linux server to gain hands-on experience with infrastructure deployment, Linux administration, and web application configuration.

The deployment simulated a real-world environment involving:

• Cloud virtual machine setup  
• Linux server configuration  
• Web server installation  
• Database configuration  
• Application deployment  
• Network security setup  

## Environment Setup

Cloud Provider:
AWS EC2

Instance Type:
t3.micro

Operating System:
Ubuntu 22.04 LTS

Access Method:
SSH using key authentication

Security Configuration:
Configured inbound rules for SSH (22) and HTTP (80).

## Deployment Process

### Server Preparation

Connected to the EC2 instance using SSH and updated system packages to ensure a secure and stable environment.

Installed required infrastructure components:

• Apache (web server)
• MariaDB (database)
• PHP (application runtime)

Restarted Apache to ensure proper service integration.

### Database Configuration

Created a dedicated WordPress database and user account to follow security best practices and avoid using root credentials.

Verified database connectivity before application installation.

### Application Installation

Downloaded WordPress into the Apache web root directory.

Configured wp-config.php to connect WordPress to the MariaDB database.

Configured file permissions to allow Apache to manage WordPress files.

Restarted Apache to apply configuration changes.

### Application Configuration

Completed WordPress browser installation.

Configured:

• Site name
• Admin credentials
• Security plugin
• Basic homepage content

## Challenges Encountered

Apache test page not loading initially due to missing HTTP security group rule.

Resolved by adding port 80 inbound rule in AWS.

SSH reconnection required after stopping instance due to public IP reassignment.

Resolved by retrieving updated public DNS from AWS console.

Database already existed after restart, confirming persistence of AWS EBS storage.

Learned how cloud storage remains intact even when compute is stopped.

## Deployment Validation

Successful deployment was confirmed by verifying:

EC2 instance running

Apache default page accessible

WordPress installation page accessible

WordPress admin dashboard accessible

Database connectivity functioning correctly

Security plugins installed

This confirmed successful end-to-end deployment.

## Key Engineering Lessons

Understanding cloud networking rules is critical for accessibility.

Linux file permissions directly impact web server behavior.

Database separation improves application security.

Stopping EC2 instances does not remove stored data.

Troubleshooting infrastructure issues requires systematic validation of networking, services, and configuration.

## Improvements for Future Iterations

Implement HTTPS using SSL certificates.

Automate deployment using shell scripts.

Containerize deployment using Docker.

Implement monitoring tools.

Create automated backups.

Use Infrastructure as Code tools such as Terraform.

## Skills Demonstrated

AWS EC2 deployment

Linux server administration

Apache configuration

Database setup and integration

WordPress deployment

Cloud networking configuration

Infrastructure troubleshooting

Technical documentation
