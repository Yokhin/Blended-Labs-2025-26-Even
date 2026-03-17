# Lab 4 – Working with Amazon Elastic Block Store (EBS)

## Author

* **Name**: Yokhin Vieshveshwar M
* **Register Number**: 212223210031
* **Date of Submission**: 17.03.2026

---

## Objective

The objective of this experiment is to understand how Amazon Elastic Block Store (EBS) provides persistent block-level storage for EC2 instances. This lab focuses on creating and attaching an EBS volume, formatting and mounting it on an EC2 instance, storing data, and verifying data persistence after instance reboot.

---

## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* An existing EC2 instance (Amazon Linux 2 preferred)
* Basic knowledge of Linux commands

---

## Tools Used

* AWS Management Console
* Amazon EC2
* Amazon EBS
* SSH Client (Terminal / PuTTY)

---

## Tasks Performed

### Task 1: Explore Amazon EBS

Explore the Amazon EBS service through the EC2 dashboard. Observe different volume types such as General Purpose SSD (gp2/gp3), Provisioned IOPS SSD, Throughput Optimized HDD, and Cold HDD.

---

### Task 2: Create an EBS Volume

Create a new EBS volume in the same Availability Zone as the EC2 instance. Choose an appropriate size and volume type.

---

### Task 3: Attach EBS Volume to EC2 Instance

Attach the created EBS volume to the running EC2 instance as an additional block device.

---

### Task 4: Format the EBS Volume

Connect to the EC2 instance using SSH and format the attached volume with a file system (for example, ext4).

---

### Task 5: Mount the EBS Volume

Mount the formatted volume to a directory in the EC2 instance (for example, /data or /mnt/ebs).

---

### Task 6: Store Data in EBS Volume

Create files and directories inside the mounted EBS volume and store sample data.

---

### Task 7: Verify Data Persistence

Reboot the EC2 instance and verify that the data stored in the EBS volume is still available after reboot.

---

## Workflow (Student Explanation)

Create a 1 GiB Amazon EBS volume in the same Availability Zone as your EC2 instance and tag it My Volume.

Attach the volume to the EC2 instance as /dev/sdf.

Connect to the instance using EC2 Instance Connect.

Format the volume with an ext3 file system and mount it to /mnt/data-store.

Update /etc/fstab to ensure the volume mounts automatically on reboot.

Create a file in the mounted volume and verify its contents.

Create a snapshot (My Snapshot) of the EBS volume, then delete the file from the original volume.

Restore the snapshot to a new volume, attach it (/dev/sdg), mount it, and verify the file is recovered.
---

## Output Screenshots (Attach 3)

### Screenshot 1: EBS Volume Created

<img width="1899" height="892" alt="Screenshot 2026-03-17 231310" src="https://github.com/user-attachments/assets/84578845-bcf1-4e29-8b69-cdc9aff17f25" />




### Screenshot 2: EBS Volume Attached to EC2

<img width="1865" height="857" alt="image" src="https://github.com/user-attachments/assets/f5042f89-b9a9-41f4-863a-acf919faa1d2" />


<img width="1613" height="354" alt="image" src="https://github.com/user-attachments/assets/0b1820c7-a6e3-4c43-a6b7-5bfd23c727b6" />


### Screenshot 3: Mounted Volume with Data

<img width="1255" height="557" alt="image" src="https://github.com/user-attachments/assets/80065f52-57da-4f82-8427-a735a02ff378" />




## Result / Conclusion

This experiment demonstrated how Amazon EBS provides persistent storage for EC2 instances. By creating, attaching, formatting, and mounting an EBS volume, and by verifying data after reboot, the concept of durable block storage in the cloud was clearly understood.
