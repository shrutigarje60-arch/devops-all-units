# Terraform: Infrastructure as Code (IaC) Guide

**Infrastructure as Code (IaC)** replaces manual provisioning processes with machine-readable definition files. **Terraform**, developed by HashiCorp, is an industry-standard declarative tool for managing cloud and on-premise infrastructure.

---

## 1. Core Concepts

* **HCL (HashiCorp Configuration Language):** A human-readable, declarative language used to describe infrastructure configurations.
* **Providers:** Plugins (e.g., AWS, Azure, GCP) that enable Terraform to interact with external cloud and service APIs.
* **State Management:** Terraform tracks resource mappings and state metadata in a `terraform.tfstate` file to reconcile configuration changes.

---

## 2. The Terraform Lifecycle Workflow

1. **`terraform init`:** Initializes the working directory, downloads required plugins, and configures backend backends.
2. **`terraform plan`:** Generates and previews an execution plan showing what changes will occur.
3. **`terraform apply`:** Executes the planned changes to reach the desired infrastructure state.
4. **`terraform destroy`:** Safely provisions and removes all resources managed by the configuration.

---

## 3. Basic HCL Configuration Example

```hcl
provider "aws" {
  region = "us-east-1"
}

resource "aws_instance" "app_server" {
  ami           = "ami-0c55b159cbfafe1f0"
  instance_type = "t2.micro"
  tags          = { Name = "Careertiq-Server" }
}
