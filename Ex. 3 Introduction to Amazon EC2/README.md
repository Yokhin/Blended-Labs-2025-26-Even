# Lab 3 – Introduction to Amazon Elastic Compute Cloud (EC2)

## Author

* **Name**: Yokhin Vieshveshwar M
* **Register Number**: 212223210031
* **Date of Submission**: 17.03.2026
---

## Objective

The objective of this experiment is to understand the fundamentals of Amazon Elastic Compute Cloud (EC2). This lab focuses on launching and managing a virtual server, understanding instance types and AMIs, connecting to an EC2 instance, monitoring its status, and performing basic instance operations such as start, stop, and terminate.

---

## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* Web browser with internet connectivity
* Basic knowledge of Linux commands (optional)

---

## Tools Used

* AWS Management Console
* Amazon EC2
* Key Pair
* Security Group
* SSH Client (PuTTY / Terminal)

---

## Tasks Performed

### Task 1: Explore Amazon EC2 Dashboard

Explore the EC2 service dashboard in the AWS Management Console. Observe the different sections such as Instances, AMIs, Instance Types, Key Pairs, Security Groups, and Elastic IPs.

---

### Task 2: Launch an EC2 Instance

Launch a new EC2 instance using Amazon Linux 2 AMI. Select an appropriate instance type (t2.micro) under the free tier. Configure basic settings such as instance name, key pair, and security group.

---

### Task 3: Configure Security Group

Configure a security group to allow inbound access:

* SSH (Port 22) from your IP address
* HTTP (Port 80) from anywhere (0.0.0.0/0)

This security group acts as a firewall for the instance.

---

### Task 4: Connect to EC2 Instance

Connect to the running EC2 instance using SSH. Use the downloaded key pair and connect via terminal or PuTTY.

For Amazon Linux:

```
ssh -i "keyname.pem" ec2-user@<Public-IP>
```

---

### Task 5: Perform Basic Instance Operations

Perform the following operations from the EC2 console:

* Stop the instance
* Start the instance
* Reboot the instance

Observe the state changes of the instance.

---

### Task 6: Monitor EC2 Instance

Monitor the EC2 instance using the Monitoring tab. Observe metrics such as CPU utilization, network in/out, and instance status checks.

---

### Task 7: Terminate EC2 Instance

Terminate the EC2 instance after completing the experiment to avoid unnecessary AWS charges.

---

## Workflow (Student Explanation)

1. I logged into the AWS Management Console and opened Amazon EC2 in the N. Virginia region. Then I launched a new instance named Web Server using the default Amazon Linux 2023 AMI and selected the t2.micro instance type with the vockey key pair.

2. I configured the network by selecting the Lab VPC and created a new security group without any inbound rules. I enabled termination protection and added a user data script to automatically install and start an Apache web server.

3. After launching the instance, I monitored its status using the Status checks and Monitoring tabs. I also viewed the system log and instance screenshot to confirm that the web server was installed correctly.

4. I copied the public IP address and tried to access the web server, but it didn’t load. Then I updated the security group by adding an HTTP (port 80) inbound rule, after which the web page displayed successfully.

5. I stopped the instance, changed its type to t2.small, enabled stop protection, and increased the EBS volume size from 8 GiB to 10 GiB. Finally, I restarted the instance and tested stop protection before completing the lab.

---

## Output Screenshots (Attach 3)

### Screenshot 1: EC2 Dashboard / Instance List

<img width="1900" height="911" alt="Screenshot 2026-03-17 221013" src="https://github.com/user-attachments/assets/1e6f0dc2-3dde-4750-8209-a7a55a84ef9c" />

<img width="1904" height="902" alt="Screenshot 2026-03-17 221655 - Copy" src="https://github.com/user-attachments/assets/6a1b0334-3ff1-4fd8-af5a-942395033d8f" />



### Screenshot 2: SSH Connection to Instance

<img width="1796" height="678" alt="Screenshot 2026-03-17 222959" src="https://github.com/user-attachments/assets/81cdcd71-d3c2-4c50-b1c9-b96bb5f298b9" />

<img width="1885" height="811" alt="Screenshot 2026-03-17 223116" src="https://github.com/user-attachments/assets/ad59541e-2f60-48ce-953c-990ee0c2f73c" />



### Screenshot 3: Instance Monitoring / Status

<img width="1654" height="775" alt="image" src="https://github.com/user-attachments/assets/d22fad6f-8c01-4b0e-957b-25f2f0dec3b6" />


## Result 

This experiment provided hands-on experience with Amazon EC2 by demonstrating how to launch, connect, manage, and monitor a virtual server in AWS. It helped in understanding the concept of Infrastructure as a Service (IaaS) and how compute resources can be provisioned and controlled on demand in the cloud.
