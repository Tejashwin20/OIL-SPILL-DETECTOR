
🌊 Oil Spill Detection Application
☁ Production-Ready AWS Deployment Package

A fully containerized, cloud-native Oil Spill Detection platform with Infrastructure as Code using Terraform, Docker-based microservices, Auto Scaling, Load Balancing, monitoring, and enterprise-grade security.

Version: 1.0
Status: Production Ready ✅
Last Updated: March 2026

🚀 What This Package Includes
🏗 Infrastructure as Code (Terraform)

✅ VPC with public & private subnets across multiple AZs

✅ RDS MySQL (Multi-AZ, automated backups)

✅ EC2 Auto Scaling Group with health checks

✅ Application Load Balancer (ALB) with HTTPS

✅ S3 bucket (encrypted, versioned, private)

✅ NAT Gateway for private subnet internet access

✅ CloudWatch monitoring & alarms

✅ IAM roles (least privilege)

✅ Security Groups with restricted access

✅ AWS Secrets Manager integration

🐳 Containerization (Docker)

✅ Dockerfiles for all 3 applications

✅ docker-compose.yml for local development

✅ Nginx reverse proxy configuration

✅ SSL/TLS support

✅ Health checks & auto-restart policies

⚙ Configuration Management

✅ .env.example environment template

✅ Centralized config.py in each application

✅ No hardcoded credentials

✅ AWS Secrets Manager for secure secrets handling

🔄 Deployment Automation

✅ Terraform automated infrastructure setup

✅ Docker-based local deployment

✅ EC2 user-data auto bootstrapping

✅ Production deployment scripts

✅ CI/CD ready structure

🏗 Architecture Overview
Internet Users
       │
       ▼
AWS Certificate Manager (HTTPS)
       │
       ▼
Application Load Balancer (ALB)
       │
       ▼
EC2 Auto Scaling Group (1–3 Instances)
       │
       ├── RDS MySQL (Multi-AZ)
       ├── S3 (Encrypted Upload Storage)
       └── CloudWatch Monitoring
🧩 Application Components
1️⃣ Oil Spill Detection API

Flask-based ML backend

PyTorch model integration

Image processing with OpenCV

2️⃣ Oil Spill Portal

User authentication (Google OAuth)

Upload interface

Dashboard view

3️⃣ Real-Time Detection Service

Continuous detection engine

Streaming/Live prediction logic

⚡ Quick Start
🐳 Option 1: Local Development (Docker)
1️⃣ Setup environment
cp .env.example .env
nano .env
2️⃣ Deploy locally
chmod +x scripts/deploy_docker.sh
./scripts/deploy_docker.sh
3️⃣ Access Applications

Oil Spill API → http://localhost:5000

Portal → http://localhost:5001

Real-Time Detection → http://localhost:5002

Nginx HTTPS → https://localhost:443

☁ Option 2: Full AWS Deployment
1️⃣ Install Required Tools

AWS CLI v2

Terraform v1.0+

Docker

2️⃣ Configure AWS
aws configure
3️⃣ Setup Infrastructure
cd terraform
cp terraform.tfvars.example terraform.tfvars
nano terraform.tfvars

terraform init
terraform plan
terraform apply
4️⃣ Deploy Application
chmod +x ../scripts/deploy.sh
../scripts/deploy.sh
5️⃣ Get Outputs
terraform output
📁 Project Structure
.
├── docker-compose.yml
├── nginx.conf
├── README.md
├── DEPLOYMENT_GUIDE.md
│
├── terraform/
│   ├── main.tf
│   ├── ec2.tf
│   ├── variables.tf
│   ├── outputs.tf
│   └── user_data.sh
│
├── scripts/
│   ├── deploy.sh
│   ├── deploy_docker.sh
│   └── production_deploy.sh
│
├── OilSpillPortal/
├── RealTimeDetection/
└── ODA(OIL)/oil_spill_detection/
🔒 Security Features

VPC network isolation

Private RDS database

IAM least privilege roles

AWS Secrets Manager

HTTPS via ACM

S3 encryption & versioning

Automated RDS backups

CloudWatch logging

Restricted security groups

📊 Monitoring & Observability
CloudWatch Dashboards

EC2 CPU utilization

RDS performance metrics

Memory usage

Network traffic

Application logs

Alerts & Alarms

High CPU

Low disk space

Unhealthy ALB targets

Failed deployments

💰 Estimated Monthly AWS Cost
Component	Type	Est. Cost
EC2	t3.medium	~$30
RDS	db.t3.small	~$50
NAT Gateway	-	~$40
Data Transfer	100GB	~$20
CloudWatch	Logs & Metrics	~$10
Total		~$150/month

Costs vary by region. Use AWS Cost Calculator for exact pricing.

📋 Pre-Deployment Checklist

AWS account configured

IAM user created

EC2 key pair created

.env configured

terraform.tfvars configured

Google OAuth credentials

Roboflow API key

AWS CLI installed

Terraform installed

Docker installed

SSH access tested

🔮 Future Improvements

CI/CD pipeline (GitHub Actions)

Kubernetes (EKS) migration

Blue/Green deployment

Model retraining pipeline

Cost optimization automation

📚 Documentation

DEPLOYMENT_GUIDE.md – Complete AWS guide

nginx.conf – Reverse proxy setup

terraform/ – Infrastructure config

scripts/ – Deployment automation

👩‍💻 Maintainer

Tejashwini Pilli

📄 License

This deployment package is developed for academic, research, and production cloud deployment use.
