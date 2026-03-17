<img width="1904" height="902" alt="Screenshot 2026-03-17 221655" src="https://github.com/user-attachments/assets/ff63bdb7-bf29-46fe-ab59-fd7d9a6cafb2" /># Lab 3 – Introduction to Amazon Elastic Compute Cloud (EC2)

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

(Write the steps you followed in your own words)

1. ---
2. ---
3. ---
4. ---
5. ---

---

## Output Screenshots (Attach 3)

### Screenshot 1: EC2 Dashboard / Instance List

<img width="1900" height="911" alt="Screenshot 2026-03-17 221013" src="https://github.com/user-attachments/assets/fe3c00b1-625f-443b-bd23-ae9078f741ae" />

<img width="1904" height="902" alt="Screenshot 2026-03-17 221655" src="https://github.com/user-attachments/assets/a5472a0a-0006-45ae-9885-6538a71fa4f2" />



### Screenshot 2: SSH Connection to Instance

<img width="1796" height="678" alt="Screenshot 2026-03-17 222959" src="https://github.com/user-attachments/assets/d2c43384-a6db-43a1-b595-1f8fe2ba7715" />

<img width="1885" height="811" alt="Screenshot 2026-03-17 223116" src="https://github.com/user-attachments/assets/163c6e83-527b-40d3-836f-e11b77e45122" />



### Screenshot 3: Instance Monitoring / Status

<img width="1654" height="775" alt="image" src="https://github.com/user-attachments/assets/dca6fe79-0fa7-4f77-8bf1-8e94b485135b" />

## Result 

This experiment provided hands-on experience with Amazon EC2 by demonstrating how to launch, connect, manage, and monitor a virtual server in AWS. It helped in understanding the concept of Infrastructure as a Service (IaaS) and how compute resources can be provisioned and controlled on demand in the cloud.
