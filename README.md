# My-first-aws-ec2-setup
This project documents my journey in setting up an **EC2 instance** on AWS.

## 🛠️ Steps Taken

1. **Created an EC2 instance** (Selected AMI, instance type, storage)
2. **Configured Security Groups** (Allowed SSH/RDP, restricted unnecessary ports)
3. **Connected to the Instance** (Using SSH for Linux or RDP for Windows)
4. **Installed & Configured Software** (e.g., Apache, Nginx, MySQL)
5. **Enabled Monitoring & Security** (CloudWatch, IAM roles, package updates)

## 🔥 Challenges & Solutions
- [Example: Faced an issue with SSH due to the wrong key pair, resolved by generating a new one.]

## 📌 Next Steps
- Automate EC2 provisioning using Terraform
- Attach an Elastic IP and configure a domain
- Explore IAM roles and networking

## 📷 Screenshots
![EC2 Instance Running](images/ec2-instance.png)

---!![Screenshot from 2025-02-16 17-22-27](https://github.com/user-attachments/assets/729347a5-a2fc-4d38-8925-e5675a363876)



### **4. (Optional) Add a Bash Script for EC2 Automation**
If you used the AWS CLI, Terraform, or CloudFormation, include a script:

```sh
#!/bin/bash
aws ec2 run-instances --image-id ami-xxxxxxxx --count 1 --instance-type t2.micro --key-name MyKeyPair --security-group-ids sg-xxxxxxxx --subnet-id subnet-xxxxxxxx
