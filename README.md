# 🚀 DevOps Workflow Implementation  
## Docker → Jenkins → AWS → Terraform → Ansible

![Docker](https://img.shields.io/badge/Step1-Docker-2496ED?style=for-the-badge&logo=docker)
![Jenkins](https://img.shields.io/badge/Step2-Jenkins-D24939?style=for-the-badge&logo=jenkins)
![AWS](https://img.shields.io/badge/Step3-AWS-FF9900?style=for-the-badge&logo=amazonaws)
![Terraform](https://img.shields.io/badge/Step4-Terraform-623CE4?style=for-the-badge&logo=terraform)
![Ansible](https://img.shields.io/badge/Step5-Ansible-EE0000?style=for-the-badge&logo=ansible)

---

# 📖 Project Overview

This project demonstrates a structured DevOps pipeline where application containerization, CI/CD automation, cloud provisioning, infrastructure as code, and configuration management are integrated into a single workflow.

The implementation follows a practical deployment strategy starting from containerization and ending with automated infrastructure configuration.

---

# 🔄 Complete DevOps Flow Explanation

---

# 🐳 Step 1: Docker – Containerization Layer

## Objective:
Package the application and its dependencies into a portable container.

## What Happens Here:

- Write a Dockerfile
- Build a Docker image
- Run the container
- Expose application via port mapping

## Example:

```bash
docker build -t myapp:v1 .
docker run -d -p 3000:3000 myapp:v1
docker ps
```

## Why Docker First?

✔ Ensures application works in isolated environment  
✔ Eliminates "works on my machine" problem  
✔ Creates production-ready container image  

Docker prepares the application for deployment.

---

# 🔁 Step 2: Jenkins – CI/CD Automation Layer

## Objective:
Automate the build and deployment process.

## What Happens Here:

- Integrate Git repository
- Automatically build Docker image
- Run build on every code commit
- Prepare deployment pipeline

## Jenkins Responsibilities:

- Continuous Integration
- Automated Docker builds
- Deployment triggering
- Pipeline execution

## Example Jenkins Flow:

1. Developer pushes code
2. Jenkins triggers build
3. Docker image is created
4. Image ready for deployment

Jenkins ensures automation and reduces manual deployment effort.

---

# ☁️ Step 3: AWS – Cloud Infrastructure Layer

## Objective:
Provide scalable cloud infrastructure to host the application.

## AWS Services Used:

- EC2 (Virtual Machine)
- Security Groups
- Key Pairs
- Public IP

AWS provides the actual server where Docker containers will run.

---

# 🏗️ Step 4: Terraform – Infrastructure as Code Layer

## Objective:
Provision AWS infrastructure automatically using code.

Instead of manually creating EC2 instances, Terraform automates it.

## Example Terraform Configuration:

```hcl
provider "aws" {
  region = "ap-south-1"
}

resource "aws_instance" "app_server" {
  ami           = "ami-xxxx"
  instance_type = "t2.micro"
}
```

## Terraform Workflow:

```bash
terraform init
terraform plan
terraform apply
```

## Why Terraform?

✔ Infrastructure automation  
✔ Reproducibility  
✔ Version-controlled cloud resources  
✔ Eliminates manual setup  

Terraform creates the AWS infrastructure where the app will run.

---

# ⚙️ Step 5: Ansible – Configuration Management Layer

## Objective:
Configure the provisioned AWS server automatically.

Once EC2 is created by Terraform, Ansible:

- Installs Docker
- Installs dependencies
- Deploys Docker container
- Starts services

## Example Playbook:

```yaml
- hosts: app
  become: yes
  tasks:
    - name: Install Docker
      apt:
        name: docker.io
        state: present
```

## Execution:

```bash
ansible-playbook setup.yml
```

## Why Ansible?

✔ Agentless automation  
✔ Remote configuration via SSH  
✔ Repeatable deployments  
✔ Faster environment setup  

Ansible prepares the AWS server to run Docker containers.

---

# 🔄 Final Integrated Workflow

1️⃣ Application is containerized using Docker  
2️⃣ Jenkins automates build process  
3️⃣ Terraform provisions AWS infrastructure  
4️⃣ Ansible configures EC2 instance  
5️⃣ Docker container runs on cloud server  

This creates a complete DevOps automation pipeline.

---

# 📌 End-to-End Architecture Flow

Developer → Git Push → Jenkins Build → Docker Image →  
Terraform Creates EC2 → Ansible Configures Server →  
Docker Container Runs on AWS → Application Live

---

# 🧠 Skills Gained

✔ Containerization  
✔ CI/CD Automation  
✔ Cloud Infrastructure Management  
✔ Infrastructure as Code  
✔ Configuration Management  
✔ Full DevOps Integration  

---

# 🎯 Conclusion

This workflow demonstrates how modern DevOps tools integrate together to automate application deployment from development to production.

Docker handles packaging,  
Jenkins handles automation,  
AWS provides infrastructure,  
Terraform provisions infrastructure,  
Ansible configures the server.

---

