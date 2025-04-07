# Create a VM instance infrastructure on Google Cloud using Terraform
Google Cloud Self-Paced Lab "Terraform Fundamentals"

## 1. Verify Terraform installation

- Google Cloud Shell: `terraform`

  [screenshot01]

## 2. Build infrastructure

### 2.1 Configuration

- Create a configuration file, e.g., `touch instance.tf`

- Open the file and add your configuration, e.g.,

  [screenshot02]

  The format of the configuration files can be found in the Terraform Language Documentation: https://www.terraform.io/docs/configuration/index.html
  
- Verify that your new file has been added and that there are no other, not required *.tf files in your directory: `ls`

### 2.2 Initialization

- Download & install provider binary: `terraform init`

  [screenshot03]

- Create an execution plan: `terraform plan`

  [screenshot04a]
  [screenshot04b]

### 2.3 Apply changes

- `terraform apply`, when prompted, confirm changes with `yes`

  [screenshot05a]
  [screenshot05b]
  
- Verify the current state: `terraform show`

  [screenshot06a]
  [screenshot06b]
  
## Project certification

[screenshot07]
