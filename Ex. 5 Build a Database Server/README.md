# Lab 5 – Build a Database Server (AWS)

## Author

* **Name**: AKASHINI V
* **Register Number**: 212225230009


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

First, I opened the AWS Management Console and went to the VPC service. I created a new security group named DB Security Group and configured it to allow MySQL (port 3306) access from the Web Security Group.

Next, I navigated to the RDS service and created a DB Subnet Group named DB-Subnet-Group. I selected the Lab VPC, chose two availability zones (us-east-1a and us-east-1b), and added the required subnets (10.0.1.0/24 and 10.0.3.0/24).

After that, I created a new Amazon RDS MySQL database instance. I selected Dev/Test template, enabled Multi-AZ deployment, and configured details like DB identifier (lab-db), username (main), and password (lab-password). I also selected db.t3.micro instance type and attached the DB Security Group.

Once the database was created, I waited until its status became available and then copied the endpoint URL from the connectivity section.

Finally, I opened the web application using the provided EC2 IP address, navigated to the RDS section, and entered the database details (endpoint, database name, username, password). After submitting, I successfully connected the app and tested it by adding and managing contacts in the address book.


---

## Output Screenshots (Attach 3)

### Screenshot 1: EC2 Instance for Database Server

<img width="1257" height="552" alt="image" src="https://github.com/user-attachments/assets/e5409fe5-9cf5-46dd-ab62-882c1fe7425c" />


---

### Screenshot 2: Database Service Running


<img width="1262" height="557" alt="image" src="https://github.com/user-attachments/assets/fdc55953-00dd-4eb6-9d01-88324cacd4cf" />

<img width="1267" height="556" alt="image" src="https://github.com/user-attachments/assets/355c1900-2370-4617-bbb0-7bc075dcf90b" />

---

### Screenshot 3: Sample Database and Table


<img width="1130" height="590" alt="image" src="https://github.com/user-attachments/assets/6364c67d-17db-4b5a-ac3d-72cc4f9e349f" />

<img width="1142" height="542" alt="image" src="https://github.com/user-attachments/assets/31fc2295-9a1b-48a8-b1c2-c87fbee82218" />


---

## Result

This experiment demonstrated how to build a database server in AWS using an EC2 instance. By installing and configuring a DBMS, creating a sample database, and testing connectivity, the fundamentals of hosting and managing a cloud-based database server were underst
