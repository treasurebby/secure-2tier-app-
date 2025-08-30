# Secure 2-Tier App Deployment (EC2 + RDS in VPC)

## 📖 Overview
This project demonstrates how to deploy and secure a **2-Tier Application** on **Amazon Web Services (AWS)** using Infrastructure as Code (Terraform/CloudFormation).

- **Frontend (Tier 1):** A simple CRUD web application hosted on **Amazon EC2** in a public subnet.
- **Backend (Tier 2):** A **managed relational database** hosted on **Amazon RDS** in a private subnet.
- Both components are deployed inside a **Virtual Private Cloud (VPC)** with proper **IAM roles, Security Groups, and subnets** for security.

This setup follows **real-world DevOps practices** by combining documentation, automation, and cloud security principles.

---

## 🎯 Learning Goals
- Understand **DevOps foundations** (repo structure, PR checklist, DoD rules).
- Learn **AWS IAM** (admin + dev users, MFA, least privilege).
- Build a **VPC with public/private subnets** using Terraform/CloudFormation.
- Deploy an **EC2 instance** for hosting a frontend app.
- Launch an **RDS database** (MySQL/Postgres) in a private subnet.
- Secure communication between EC2 → RDS with **Security Groups**.
- Document everything (runbook, diagrams, blog post).

---

## 🛠️ Architecture
User (Browser)
│
[ Internet ]
│
┌──────────────┐
│ EC2 (App) │ → Public Subnet
└──────────────┘
│
┌──────────────┐
│ RDS (DB) │ → Private Subnet
└──────────────┘
- EC2 instance is **publicly accessible** (via HTTP/SSH).
- RDS database is **private** (only EC2 can connect).
- All resources live inside a **custom VPC**.

---

## 🧰 Tech Stack
- **AWS Services:** EC2, RDS, VPC, IAM, Security Groups
- **IaC (Infrastructure as Code):** Terraform or CloudFormation
- **App:** Simple CRUD app (Node.js or Python Flask)
- **Database:** Amazon RDS (MySQL/Postgres)
- **Docs:** Architecture diagram, runbook, learning notes

---

## 📂 Repository Structure
secure-2tier-app/
├── app/ # Web app code (CRUD)
├── infra/ # Terraform/CF templates
├── docs/ # Architecture, runbook, blog draft
├── .github/ # PR checklist, workflows
└── README.md # Project description


---

## ✅ Deliverables
- Working **2-tier application** on AWS
- Infrastructure deployed via **Terraform/CloudFormation**
- Security implemented with **IAM, VPC, and SGs**
- Documentation:
  - Architecture diagram
  - Runbook (how to operate the app)
  - Blog post draft
