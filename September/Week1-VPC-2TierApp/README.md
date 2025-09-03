# 🏗️ Week 1 – Secure 2-Tier App on AWS VPC

## 📌 Goal
Design and deploy a **secure two-tier web application** in AWS using a custom VPC, subnets, and security groups.

---

## 🛠️ Architecture
- **VPC** with public and private subnets  
- **Internet Gateway** for public access  
- **NAT Gateway** for private subnet outbound traffic  
- **EC2 Web Server** in the public subnet  
- **EC2 Database Server** in the private subnet  
- **Security Groups** to allow only necessary traffic  

📂 *See [diagrams/](diagrams/) for architecture diagram*

---

## 🚀 Steps
1. Create a new VPC (`10.0.0.0/16`)  
2. Add 2 subnets: Public (`10.0.1.0/24`) and Private (`10.0.2.0/24`)  
3. Attach an Internet Gateway to the VPC  
4. Create a NAT Gateway in the Public subnet  
5. Launch a **Web EC2** in Public subnet (Ubuntu, Apache/NGINX)  
6. Launch a **DB EC2** in Private subnet (MySQL/Postgres)  
7. Configure Security Groups:  
   - Web SG → Allow HTTP/HTTPS (0.0.0.0/0)  
   - DB SG → Allow MySQL/Postgres (only from Web SG)  
8. Test connectivity between Web and DB  

---

## 📸 Screenshots
- VPC Dashboard → [screenshots/vpc-dashboard.png](screenshots/vpc-dashboard.png)  
- EC2 Web Server running → [screenshots/web-ec2.png](screenshots/web-ec2.png)  

---

## ✅ Results
- Successfully deployed a **secure 2-tier app** on AWS  
- Verified web-to-db connectivity inside VPC  
- All security rules followed *least privilege principle*  

---

## 📚 Learning Outcomes
- Understood **VPC networking basics** (CIDR, subnets, gateways)  
- Practiced **EC2 + Security Group configuration**  
- Learned how to isolate private workloads (DB) from the internet  

---

👨‍💻 Author: Francis Mwendwa

