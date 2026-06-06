<div align="center">

# Secure CI/CD Pipeline for Static Website on AWS

![AWS](https://img.shields.io/badge/AWS-Cloud-orange?style=flat-square)
![GitHub](https://img.shields.io/badge/GitHub-Source%20Control-black?style=flat-square)
![CodePipeline](https://img.shields.io/badge/AWS%20CodePipeline-CI%2FCD-blue?style=flat-square)
![CodeBuild](https://img.shields.io/badge/AWS%20CodeBuild-Build-green?style=flat-square)
![Amazon S3](https://img.shields.io/badge/Amazon%20S3-Static%20Hosting-yellow?style=flat-square)
![CloudFront](https://img.shields.io/badge/CloudFront-CDN-lightgrey?style=flat-square)
![AWS WAF](https://img.shields.io/badge/AWS%20WAF-Security-red?style=flat-square)
![ACM](https://img.shields.io/badge/ACM-HTTPS%2FSSL-success?style=flat-square)
![GitHub license](https://img.shields.io/github/license/githubWithGHANA/aws-devsecops-ci-cd-pipeline?style=flat-square)
</div>

## Overview
This project implements a **secure, automated CI/CD pipeline** to deploy a static web application (HTML, CSS, JavaScript) from **GitHub to AWS Cloud**.  
The pipeline uses **AWS CodePipeline** and **AWS CodeBuild** for automation, **Amazon S3** for hosting, **Amazon CloudFront** for content delivery, and **AWS WAF** with **ACM** for security and HTTPS.

The solution follows **AWS and DevOps best practices** and is suitable for production-grade static website deployments.

---

## Architecture
**Flow:**

CI/CD Flow:
```
GitHub → CodePipeline → CodeBuild → Amazon S3
```

Runtime Flow:
```
End Users → CloudFront → Amazon S3
               ↑
            AWS WAF

```

---

## AWS Services Used
- GitHub (Source Control)
- AWS CodePipeline (CI/CD Orchestration)
- AWS CodeBuild (Build & Artifact Generation)
- Amazon S3 (Static Website Hosting)
- Amazon CloudFront (Content Delivery Network)
- AWS WAF (Web Application Firewall)
- AWS Certificate Manager (SSL/TLS)
- AWS IAM (Access Management)
- AWS CloudWatch (Logging & Monitoring)

---

## CI/CD Workflow
1. Code is pushed to the GitHub repository.
2. AWS CodePipeline is triggered automatically.
3. AWS CodeBuild:
   - Executes build instructions
   - Prepares static files as build artifacts
4. Artifacts are deployed to an Amazon S3 bucket.
5. CloudFront serves the content globally with low latency.
6. AWS WAF filters malicious traffic.
7. HTTPS is enforced using ACM certificates.

---

## Security Implementation
- S3 bucket access restricted to CloudFront only
- Web traffic protected using AWS WAF managed rules
- HTTPS enabled via AWS Certificate Manager
- IAM roles configured with least-privilege access
- No direct public access to S3 resources

---

## Deployment Model
- **Deployment Type:** Fully automated
- **Rollback:** Supported via CodePipeline
- **Scalability:** Managed by CloudFront and S3
- **Availability:** High availability using AWS global infrastructure

---

## Use Cases
- Secure static website hosting
- DevOps CI/CD demonstration project
- AWS DevOps resume and interview showcase
- Cloud security implementation example

---
---

## Frontend Template Attribution
This project uses a pre-built frontend template with the following details:

- **Template Name:** CHEFER – Chef Website Template  
- **Template Author:** HTML Codex  
- **Author Website:** https://htmlcodex.com  
- **Template Link:** https://htmlcodex.com/chef-website-template  
- **Template License:** https://htmlcodex.com/license  

All credit for the frontend design belongs to the original author.  
The DevOps CI/CD pipeline, AWS architecture, and security implementation are independently designed and implemented.

---
## Project Ownership
This project was implemented as part of a live AWS DevOps workshop focused on **CI/CD automation and security best practices**.

---

## License
This project is for educational and demonstration purposes.
---