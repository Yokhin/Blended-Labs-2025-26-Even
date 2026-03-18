# Lab 5 – Build a Database Server (AWS)

## Author

* **Name**: Yokhin Vieshveshwar M
* **Register Number**: 212223210031
* **Date of Submission**: 18.03.2026

---

## Objective

The objective of this experiment is to understand how to deploy and configure a database server in AWS. This lab focuses on launching an EC2 instance, installing a database management system (DBMS), configuring basic database settings, creating a sample database, and validating connectivity to the database server.

---

## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* An existing VPC and EC2 knowledge (from previous labs)
* Basic knowledge of Linux commands and SQL

---

## Tools Used

* AWS Management Console
* Amazon EC2
* Security Groups
* SSH Client (Terminal / PuTTY)
* MySQL / MariaDB / PostgreSQL (any one)

---

## Tasks Performed

### Task 1: Launch EC2 Instance for Database Server

Launch a new EC2 instance using Amazon Linux 2 AMI. Select an appropriate instance type and configure key pair and security group.

---

### Task 2: Configure Security Group for Database Access

Modify the security group to allow:

* SSH (Port 22) for remote access
* Database port (e.g., MySQL – 3306 or PostgreSQL – 5432)

---

### Task 3: Connect to EC2 Instance

Connect to the EC2 instance using SSH from your local machine.

---

### Task 4: Install Database Server

Install a database server software such as MySQL, MariaDB, or PostgreSQL on the EC2 instance using package manager commands.

---

### Task 5: Start and Configure Database Service

Start the database service and configure basic settings such as root password and user privileges.

---

### Task 6: Create a Sample Database

Create a sample database and a table inside it. Insert a few records into the table.

---

### Task 7: Test Database Connectivity

Test the database server by connecting to it locally or remotely and performing basic SQL queries.

---

## Workflow (Student Explanation)

Go to AWS Console → VPC → Create Security Group (DB Security Group in Lab VPC).

Add inbound rule: MySQL (3306) → Source = Web Security Group → Create.

Go to RDS → Subnet Groups → Create DB Subnet Group.

Select Lab VPC, choose 2 AZs (us-east-1a & us-east-1b) and their subnets → Create.

Go to RDS → Databases → Create database (MySQL, Dev/Test, Multi-AZ).

Configure DB: name (lab-db), username (main), password, db.t3.micro, 20GB storage.

Set connectivity: Lab VPC + DB Security Group, disable monitoring/backups/encryption → Create DB.

Wait until DB is available → Copy the Endpoint.

Open Web Server IP → go to RDS page → enter endpoint, DB name, username & password → Submit.

Test the app (add/edit/delete contacts) to confirm database is working.


## Output Screenshots (Attach 3)

### Screenshot 1: EC2 Instance for Database Server

<img width="1265" height="577" alt="image" src="https://github.com/user-attachments/assets/39a14cf2-bb36-4cba-ac6b-58c8610b9e4f" />


### Screenshot 2: Database Service Running

<img width="1238" height="572" alt="image" src="https://github.com/user-attachments/assets/080af17e-1b48-462f-a5f5-19bb1fe23a24" />


### Screenshot 3: Sample Database and Table

<img width="1255" height="430" alt="image" src="https://github.com/user-attachments/assets/f50f28ee-5c48-4b08-91a9-9bbc51a8a1f5" />


## Result

This experiment demonstrated how to build a database server in AWS using an EC2 instance. By installing and configuring a DBMS, creating a sample database, and testing connectivity, the fundamentals of hosting and managing a cloud-based database server were underst
