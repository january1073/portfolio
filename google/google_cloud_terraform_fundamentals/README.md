# Create a VM instance infrastructure on Google Cloud using Terraform
Google Cloud Self-Paced Lab "Terraform Fundamentals"

## 1. Verify Terraform installation

- Google Cloud Shell: `terraform`

  ![screenshot](https://github.com/january1073/portfolio/blob/main/google/google_cloud_terraform_fundamentals/screenshot01.png)
  
## 2. Build infrastructure

### 2.1 Configuration

- Create a configuration file, e.g., `touch instance.tf`

- Open the file and add your configuration, e.g.,

  ![screenshot](https://github.com/january1073/portfolio/blob/main/google/google_cloud_terraform_fundamentals/screenshot02.png)

  The format of the configuration files can be found in the Terraform Language Documentation: https://www.terraform.io/docs/configuration/index.html
  
- Verify that your new file has been added and that there are no other, not required *.tf files in your directory: `ls`

### 2.2 Initialization

- Download & install provider binary: `terraform init`

  ![screenshot](https://github.com/january1073/portfolio/blob/main/google/google_cloud_terraform_fundamentals/screenshot03.png)

- Create an execution plan: `terraform plan`

  ![screenshot](https://github.com/january1073/portfolio/blob/main/google/google_cloud_terraform_fundamentals/screenshot04a.png)
  ![screenshot](https://github.com/january1073/portfolio/blob/main/google/google_cloud_terraform_fundamentals/screenshot04b.png)

### 2.3 Apply changes

- `terraform apply`, when prompted, confirm changes with `yes`

  ![screenshot](https://github.com/january1073/portfolio/blob/main/google/google_cloud_terraform_fundamentals/screenshot05a.png)
  ![screenshot](https://github.com/january1073/portfolio/blob/main/google/google_cloud_terraform_fundamentals/screenshot05b.png)
  
- Verify the current state: `terraform show`

  ![screenshot](https://github.com/january1073/portfolio/blob/main/google/google_cloud_terraform_fundamentals/screenshot06a.png)
  ![screenshot](https://github.com/january1073/portfolio/blob/main/google/google_cloud_terraform_fundamentals/screenshot06b.png)
  
## Project certification

![screenshot](https://github.com/january1073/portfolio/blob/main/google/google_cloud_terraform_fundamentals/screenshot07.png)
