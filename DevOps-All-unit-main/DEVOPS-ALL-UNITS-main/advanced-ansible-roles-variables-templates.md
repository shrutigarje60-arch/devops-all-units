# Advanced Ansible: Roles, Variables, and Templates

Mastering advanced Ansible concepts enables scalable, reusable, and dynamic infrastructure automation through structured roles, precise variable scoping, and powerful Jinja2 templating.

---

## 1. Writing Ansible Roles

Roles provide a standardized framework for modular, independent, and reusable automation units, making it easy to share workflows across projects and teams.

### Standard Role Directory Structure
```text
roles/role_name/
├── defaults/  # Default variables (lowest priority)
├── vars/      # Role-specific variables (high priority)
├── tasks/     # Main list of executable tasks
├── handlers/  # Handlers triggered by tasks
├── templates/ # Jinja2 templates used by the role
├── files/     # Static files deployed by the role
└── meta/      # Role metadata (dependencies, author information)
