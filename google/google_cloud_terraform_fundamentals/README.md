# Terraform Fundamentals
Google Cloud Self-Paced Labs

## 1. Verify Terraform installation

- Google Cloud Shell: `terraform`

## 2. Build infrastructure

### 2.1 Configuration

- Create a configuration file, e.g., `touch instance.tf`

- Open the file and add your configuration, e.g.,

  [screenshot]

  The format of the configuration files can be found in the Terraform Language Documentation: https://www.terraform.io/docs/configuration/index.html
  
- Verify that your new file has been added and that there are no other, not required *.tf files in your directory, `ls`

### 2.2 Initialization

- Download & install provider binary: `terraform init`

- Create an execution plan: `terraform plan`

### 2.3 Apply changes

- `terraform apply`, when prompted, confirm changes with `yes`

- Verify the current state: `terraform show`

## Project certification

[screenshot]
