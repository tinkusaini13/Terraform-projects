# Terraform AWS S3 Static Website Hosting

# Project Description:

- In this project, I developed a streamlined infrastructure for hosting a static website using Terraform and Amazon Web Services (AWS) S3. The primary goal of this project is to demonstrate the automated provisioning and deployment of a web hosting solution for static websites.

# Workflow:
![workflow](https://github.com/tinkusaini13/Terraform-projects/assets/88707521/33f04105-039f-4052-80a6-0bd1d870fd63)


# Key Components and Features:

# Terraform Infrastructure as Code (IaC):

I utilized Terraform, an IaC tool, to define and provision the AWS resources required for my static website hosting solution. This allows for version-controlled, repeatable infrastructure deployments.

# AWS S3 Bucket:
I created an S3 bucket to store and serve the static website files. This bucket is configured for website hosting, allowing for easy content delivery.

# Content Upload and Management:
I provided instructions and scripts for uploading and managing my website content within the S3 bucket.

# Steps :

Step 1: Set Up Your Development Environment

    aws configure

Step 2: Define Your Website Content

    index.html
    error.html

Step 3: Terraform Configuration File Syntax

- Create terraform files for s3 bucket create and upload the website source code.

    resource.tf

    provider.tf


Step 4: Define output variable for s3 endpoint url to access website.

    output "websiteendpoint" {
    value = aws_s3_bucket.bucket1.website_endpoint
    }

Step 5:Terraform to provisioning the resources

    terraform init
    terraform plan
    terraform apply -auto-approve

Step 6: Verify the Output

        
- aws_s3_bucket.bucket1 has changed

        web-bucket-pro1.s3-website.ap-south-1.amazonaws.com

Step 7: Destroy the all resources

    terraform destroy --auto-approve
