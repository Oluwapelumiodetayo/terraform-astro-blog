# Astro Blog Deployment with Terraform (AWS S3 + CloudFront)

## Overview

This project is a real-world Infrastructure as Code (IaC) deployment of a static Astro blog using Terraform on AWS. It provisions and manages an S3 bucket for hosting static files and a CloudFront distribution for global content delivery.

The site is currently live and accessible via AWS CloudFront.

---

## Live Website

CloudFront URL:
```
https://ddbqgnp3himrp.cloudfront.net
```

S3 Bucket:
```
my-terraform-site-2026-oluwapelumi
```

---

## What I Built

I deployed a static Astro blog using Terraform by:

- Creating an AWS S3 bucket for static hosting
- Uploading the Astro build output to S3
- Configuring S3 bucket policies for public access
- Setting up a CloudFront distribution for CDN delivery
- Managing all infrastructure using Terraform
- Automating deployment using IaC principles

---

## Architecture

Astro Build → S3 Bucket → CloudFront CDN → Internet Users

---

## Tech Stack

- Terraform
- AWS S3
- AWS CloudFront
- Astro
- Linux (Ubuntu)
- Git & GitHub

---

## Terraform Workflow Used

```bash
terraform init
terraform plan
terraform apply
terraform destroy
terraform apply
```

This confirmed that the infrastructure is fully reproducible.

---

## Key Outputs from Terraform

```hcl
cloudfront_url = "ddbqgnp3himrp.cloudfront.net"
s3_bucket_name = "my-terraform-site-2026-oluwapelumi"
```

---

## Key Learnings

- Infrastructure as Code ensures repeatable deployments
- CloudFront improves performance and global access
- S3 can serve static websites at scale
- Terraform state tracks real AWS infrastructure
- Plan → Apply → Destroy cycle validates reliability

---

## Notes

- Terraform state files are excluded from GitHub
- CloudFront deployment may take a few minutes to propagate
- All infrastructure is fully managed via Terraform
