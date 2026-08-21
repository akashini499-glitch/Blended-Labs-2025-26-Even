# Lab 3 – Introduction to Amazon Elastic Compute Cloud (EC2)

## Author

* **Name**: AKASHINI V
* **Register Number**: 212225230009


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

First, I logged in to the AWS Management Console using my AWS account.

I searched for EC2 in the services section and opened the EC2 Dashboard.

I explored different sections like Instances, AMIs, Instance Types, Key Pairs, Security Groups, and Elastic IPs to understand their functions.

I clicked on the “Launch Instance” button to create a new EC2 instance.

I selected Amazon Linux 2 AMI as the operating system.

I chose the t2.micro instance type because it is eligible for the AWS Free Tier.

I entered a name for my instance to identify it easily.

I created a new key pair, selected the PEM format, and downloaded it to my system.

I configured the security group settings.

I allowed SSH access on Port 22 only from my IP address.

I allowed HTTP access on Port 80 from anywhere (0.0.0.0/0).

I reviewed all the configurations and clicked on “Launch Instance.”

After launching, I waited until the instance state changed to “Running.”

I copied the public IP address of the instance from the EC2 dashboard.

I opened the terminal and navigated to the folder where the key pair file was saved.

I connected to the instance using the SSH command: ssh -i "keyname.pem" ec2-user@

I successfully logged in to the Amazon Linux server.

I went back to the EC2 console and selected the instance.

I clicked on “Stop” and observed the instance state changing to “Stopped.”

I clicked on “Start” and observed the state changing back to “Running.”

I also performed the “Reboot” operation and noticed that the instance restarted.

I opened the “Monitoring” tab to check CPU utilization and network metrics.

I observed the status checks to ensure the instance was running properly.

After completing the experiment, I selected the instance and clicked on “Terminate.”

I confirmed the termination and observed that the instance state changed to “Terminated.”
## Output Screenshots (Attach 3)

### Screenshot 1: EC2 Dashboard / Instance List

<img width="1919" height="982" alt="Screenshot 2026-08-17 133454" src="https://github.com/user-attachments/assets/f787dad0-dbd3-4e50-ba45-6b0df0ef68b8" />


### Screenshot 2: SSH Connection to Instance

<img width="1919" height="982" alt="Screenshot 2026-08-17 135752" src="https://github.com/user-attachments/assets/682c58de-a39b-4bde-83c3-85f93e15728b" />


<img width="1918" height="980" alt="Screenshot 2026-08-17 135904" src="https://github.com/user-attachments/assets/c57ff7d9-ee28-4210-ae1b-c62c7bc44990" />

<img width="1424" height="917" alt="Screenshot 2026-08-17 141006" src="https://github.com/user-attachments/assets/759caa50-c40a-48d6-8338-7a4c86a4aac2" />



### Screenshot 3: Instance Monitoring / Status


<img width="1919" height="977" alt="Screenshot 2026-08-17 141526" src="https://github.com/user-attachments/assets/4e8f25be-db0d-4a36-b1a5-4c6afcb17433" />


<img width="1919" height="925" alt="Screenshot 2026-08-17 142033" src="https://github.com/user-attachments/assets/ef7a20c0-c50a-4834-a218-ed9cfc610f27" />

<img width="1919" height="871" alt="Screenshot 2026-08-17 142506" src="https://github.com/user-attachments/assets/6fa5aa4c-837d-482d-a910-c4485b6b4a04" />


## Result 

This experiment provided hands-on experience with Amazon EC2 by demonstrating how to launch, connect, manage, and monitor a virtual server in AWS. It helped in understanding the concept of Infrastructure as a Service (IaaS) and how compute resources can be provisioned and controlled on demand in the cloud.
