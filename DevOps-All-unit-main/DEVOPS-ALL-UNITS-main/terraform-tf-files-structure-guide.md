# Managing Infrastructure with .tf Files: Deep Dive into Terraform Configuration

Terraform uses declarative configuration files ending in `.tf` written in **HashiCorp Configuration Language (HCL)** to define and provision target infrastructure states.

---

## 1. Anatomy of `.tf` Files

* **Declarative Approach:** Files describe the final desired state rather than sequential commands.
* **Global Loading:** All `.tf` files within a working directory are automatically loaded, merged, and evaluated together, regardless of their internal order.
* **Commenting Syntax:** Single-line comments use `#` or `//`; block comments use `/* ... */`.

---

## 2. Essential HCL Block Types

* **`terraform` Block:** Configures core Terraform settings, required versions, and remote state backends.
* **`provider` Block:** Configures target cloud providers (e.g., AWS, Azure, GCP) and authentication parameters.
* **`resource` Block:** Declares specific infrastructure components (e.g., virtual machines, networks, security groups).

---

## 3. Recommended Project File Organization

For professional enterprise projects (such as Careertiq standards), configurations are cleanly divided into modular files:

* **`main.tf`:** Primary resource definitions and infrastructure logic.
* **`variables.tf`:** Declarations and type constraints for input variables.
* **`outputs.tf`:** Data values exported and displayed after a successful `apply`.
* **`providers.tf`:** Cloud provider setups and version constraints.
* **`terraform.tfvars`:** Concrete assignment values for input variables.

---

## 4. Practical Configuration Example

### `variables.tf`
```hcl
variable "instance_name" {
  type    = string
  default = "Careertiq-Instance"
}
