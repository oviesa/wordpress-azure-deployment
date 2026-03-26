# Deployment Steps

## Project: WordPress Cloud Deployment on AWS EC2

This document outlines the steps used to deploy a WordPress website on an AWS EC2 Ubuntu server using Apache, MariaDB, and PHP.

---

## 1. Launch EC2 Instance

- Logged into AWS Console
- Navigated to EC2
- Launched a new instance named `wordpress-server`
- Selected **Ubuntu Server 22.04 LTS**
- Chose instance type **t3.micro**
- Created and downloaded SSH key pair
- Configured security group rules:
  - SSH (22)
  - HTTP (80)
  - HTTPS (443)

---

## 2. Connect to the Server

Connected to the EC2 instance using SSH:

```bash
ssh -i wordpress-key.pem ubuntu@<public-dns>
