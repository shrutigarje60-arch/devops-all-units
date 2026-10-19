# Ansible Basics: Installation, Playbooks, and Inventory Management

**Ansible** is an open-source, agentless IT automation engine used for application deployment, cloud provisioning, configuration management, and multi-tier orchestration.

---

## 1. Key Features

* **Agentless:** Operates via SSH or WinRM without installing software/agents on managed target nodes.
* **Declarative YAML:** Configuration playbooks are authored in readable, structured YAML.
* **Idempotency:** Applying a playbook repeatedly ensures the system remains in the desired state without unwanted side effects.

---

## 2. Installation (Control Node)

Ansible is installed only on the **Control Node**, which manages external target systems.

### Ubuntu / Debian
```bash
sudo apt update
sudo apt install software-properties-common
sudo add-apt-repository --yes --update ppa:ansible/ansible
sudo apt install ansible
