# Terraform Astro Blog Deployment (S3 + CloudFront)

This project demonstrates a full Infrastructure as Code (IaC) deployment of a static Astro blog using Terraform on AWS. It provisions an S3 bucket for static hosting and a CloudFront distribution for global CDN delivery.

The goal is to create a fully repeatable, production-style deployment using Terraform.

## Stack
Terraform, AWS S3, CloudFront, Astro, Linux, Git

## What it does
- Builds Astro static site into /dist
- Uploads files to AWS S3
- Serves content via CloudFront CDN
- Manages infrastructure using Terraform

## Deployment

Initialize Terraform
```bash
terraform init
```

Plan infrastructure
```bash
terraform plan
```

Apply infrastructure
```bash
terraform apply
```

Confirm with:
```bash
yes
```

## Build and upload site

Build Astro project
```bash
npm run build
```

Upload to S3
```bash
aws s3 sync dist/ s3://YOUR_BUCKET_NAME
```

## Test full lifecycle

Destroy infrastructure
```bash
terraform destroy
```

Recreate infrastructure
```bash
terraform apply
```

This confirms infrastructure is fully reproducible.

## Outputs
- CloudFront URL (main website endpoint)
- S3 bucket name

Example:
cloudfront_url = dxxxxx.cloudfront.net

## Key learning
- Infrastructure is code, not manual setup
- Terraform ensures reproducibility
- CloudFront improves global performance
- State file tracks real-world infrastructure

## Notes
- Do not commit terraform.tfstate
- Do not commit .terraform folder
- Always run terraform plan before apply
