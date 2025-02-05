# Full-Stack Website Development & AWS Deployment  

This repository documents the **end-to-end development and deployment** of a **dynamic website**, covering **frontend and backend development**, along with **cloud hosting on AWS** for **high availability, security, and scalability**.  

## Table of Contents  
- [Introduction](#introduction)  
- [Website Development](#website-development)  
- [Cloud Architecture Overview](#cloud-architecture-overview)  
- [AWS Services Used](#aws-services-used)  
- [Step-by-Step Deployment](#step-by-step-deployment) 


## Introduction  
This project was carried out as part of an **internship at IngePro Maroc**, an **engineering firm specializing in infrastructure execution studies**.  
The primary objectives were:  
**Develop a fully functional, responsive website** to showcase company projects.  
**Implement cloud deployment on AWS** for scalability, security, and high performance.  


## Website Development  
The website was built using:  
- **Frontend:** HTML, CSS, JavaScript, Bootstrap  
- **Backend:** PHP, MySQL, PHPMyAdmin  
- **Security & Authentication:** Session-based login for admin access  
- **Key Features:**  
  - Dynamic **client contact management**  
  - Interactive **project portfolio display**  
  - **Newsletter system** for customer engagement  


## Cloud Architecture Overview  
The website was deployed using **AWS cloud infrastructure**, following a **three-tier architecture**:  
1**Frontend Layer** → Hosted on **Amazon EC2 (Apache server)**.  
2**Backend Layer** → Runs PHP and MySQL on **RDS (Managed Database)**.  
3**Storage Layer** → Static assets are stored in **Amazon S3**.  
4**Domain Name & DNS Management** → Handled by **AWS Route 53**. 


## AWS Services Used  
### **1 Compute & Networking**  
- **Amazon EC2** → Hosts the PHP website.  
- **AWS VPC** → Manages private networking.  
- **AWS Route 53** → Maps domain names to AWS resources.  
- **Application Load Balancer (ALB)** → Distributes traffic across instances.  

### **2 Storage & Database**  
- **Amazon S3** → Stores website assets and documents.  
- **Amazon RDS (MySQL)** → Managed relational database.  

### **3 Security & Access Management**  
- **AWS IAM** → Role-based access control.  
- **AWS Certificate Manager (ACM)** → SSL/TLS encryption.  
- **Security Groups** → Protect EC2 instances from unauthorized access.  


## Step-by-Step Deployment  
### **1 Setting Up AWS Infrastructure**  
1. **Create a VPC** with separate public and private subnets.  
2. **Deploy an EC2 instance** to host the website.  
3. **Set up an RDS MySQL instance** for database management.  

### **2 Configuring Amazon RDS (MySQL)**  
- **Provision a `db.t3.micro` instance** with automated backups.  
- **Connect EC2 to RDS** using secure credentials.  

### **3 Hosting Static Content on Amazon S3**  
- **Upload all assets** (images, PDFs, HTML files ...) to S3.  
- **Use AWS CLI for automation**:  
  ```bash
  aws s3 cp assets/ s3://my-bucket-name/ --recursive

### **4 Configuring Route 53 for Domain Name**
To give the website a custom domain name, follow these steps:
1. **Register a domain name** in AWS Route 53.
2. **Create a hosted zone** to manage DNS records.
3. **Create an A record** to map the domain to the Application Load Balancer (ALB).
4. **Enable HTTPS** with ACM for security.

### **FOR A DETAILED GUIDE, FOLLOW STEP BY STEP GUIDE (PDF) **
