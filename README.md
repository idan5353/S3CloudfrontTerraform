# 🌐 Static Website Deployment with AWS CloudFront and S3 using Terraform 🚀

## Overview

This project demonstrates how to deploy a static website using AWS S3 for storage and CloudFront for distribution, all managed with Terraform. The `main.tf` file includes the configuration for creating an S3 bucket, enabling static website hosting, and setting up a CloudFront distribution for global content delivery.

## Prerequisites

Before you begin, ensure you have the following:

- **AWS CLI** installed and configured. [Install AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2.html) 🌟
- **Terraform** installed. [Install Terraform](https://learn.hashicorp.com/terraform/getting-started/install) ⚙️
- An **AWS account**. 🏗️

## Project Structure

- `main.tf`: Terraform configuration file for setting up S3, CloudFront, and related resources. 📄

## Setup

1. **Clone the repository:**

    ```bash
    git clone https://github.com/your-username/static-website-cloudfront.git
    cd static-website-cloudfront
    ```

2. **Configure AWS Credentials:**

    Ensure your AWS CLI is configured with the necessary credentials:

    ```bash
    aws configure
    ```

3. **Initialize Terraform:**

    Navigate to the project directory and initialize Terraform:

    ```bash
    terraform init
    ```

4. **Plan the Terraform Deployment:**

    Review the changes Terraform will make to your infrastructure:

    ```bash
    terraform plan
    ```

5. **Apply the Terraform Configuration:**

    Deploy the infrastructure:

    ```bash
    terraform apply
    ```

    Confirm the action when prompted. ✅

6. **Upload Static Website Files:**

    Place your static website files (e.g., `index.html`, `styles.css`, `app.js`) in the `content/` directory. Terraform will automatically upload these files to the S3 bucket.

    Example directory structure:

    ```
    content/
    ├── index.html
    ├── styles.css
    └── app.js
    ```

7. **Access Your Website:**

    Once the deployment is complete, you can access your website via the CloudFront distribution URL. Check the following outputs for access:

    - **Website URL (HTTPS):** The URL provided by CloudFront. 🌐
    - **S3 Hosting URL (HTTP):** The direct URL to your S3 bucket (useful for debugging). 🔗

    You can find these URLs in the Terraform outputs after running `terraform apply`.

## Cleanup

To remove all resources created by Terraform, use:

```bash
terraform destroy
