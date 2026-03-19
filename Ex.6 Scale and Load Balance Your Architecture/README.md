# Lab 6 – Scale and Load Balance Your Architecture

## Title

Scale and Load Balance Your Architecture
Author : Yokhin Vieshveshwar M   Reg no : 212223210031   Date : 19.03.2026

---

## Objective

The objective of this lab is to understand how to design a scalable and highly available architecture on AWS using Auto Scaling and Elastic Load Balancing. This experiment focuses on distributing incoming traffic across multiple EC2 instances, automatically scaling resources based on demand, and validating fault tolerance.

---

## Prerequisites

* Basic knowledge of Amazon EC2 and VPC
* Completion of previous labs (IAM, EC2, EBS, Database Server)
* AWS Academy Lab access
* Stable internet connection

---

## Tools Used

* AWS Management Console
* Amazon EC2
* Elastic Load Balancer (ELB / ALB)
* Auto Scaling Groups (ASG)
* Amazon CloudWatch

---

## Tasks Performed

### Task 1: Review Existing Architecture

Students review the existing EC2-based application architecture created in previous experiments.

### Task 2: Create a Launch Template

Students create a launch template that defines the EC2 instance configuration including AMI, instance type, security group, and user data.

### Task 3: Create an Auto Scaling Group

Students create an Auto Scaling Group using the launch template and configure minimum, maximum, and desired instance capacity.

### Task 4: Configure an Application Load Balancer

Students create an Application Load Balancer and configure target groups for routing traffic to EC2 instances.

### Task 5: Register Auto Scaling Group with Load Balancer

Students attach the Auto Scaling Group to the target group of the load balancer.

### Task 6: Configure Scaling Policies

Students configure scaling policies based on CPU utilization using Amazon CloudWatch alarms.

### Task 7: Test Load Balancing and Scaling

Students test the setup by generating traffic and observing automatic scaling and load distribution.

---

## Workflow (To be filled by Student)

Go to EC2 → Instances → select Web Server 1 → create AMI (WebServerAMI).

Go to Target Groups → create target group (LabGroup in Lab VPC).

Go to Load Balancers → create Application Load Balancer (LabELB) with public subnets and Web Security Group → attach LabGroup.

Go to Launch Templates → create template (LabConfig) using WebServerAMI, t2.micro, key pair, Web Security Group.

Create Auto Scaling Group using template → select Lab VPC + private subnets.

Attach Auto Scaling Group to LabGroup (load balancer).

Set capacity: min 2, desired 2, max 6 + scaling policy (CPU ~60%).

Verify: check instances and target group → ensure instances are healthy → test using Load Balancer DNS.

Perform load test → monitor CloudWatch alarms → confirm new instances launch automatically.

Terminate Web Server 1.

## Output Screenshots 

## Load Balancer
<img width="1898" height="867" alt="image" src="https://github.com/user-attachments/assets/3c7460e5-c977-45b6-8517-c2b2441070de" />

## Auto Scaling
<img width="1920" height="967" alt="image" src="https://github.com/user-attachments/assets/cff35868-a985-4031-9984-610a6ebde5c2" />

## Result
The lab successfully demonstrated a highly available and scalable web application using an AMI, Application Load Balancer, and Auto Scaling Group that automatically adjusts instances based on demand.


This experiment demonstrated how to build a scalable and fault-tolerant cloud architecture using Auto Scaling Groups and Elastic Load Balancing. The system automatically adjusted resources based on workload and ensured continuous service availability by distributing traffic across multiple instances.
