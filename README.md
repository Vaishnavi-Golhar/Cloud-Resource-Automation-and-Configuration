# ⚙️ Configuration Management with Terraform & Ansible

## 📝 Project Description

This project demonstrates infrastructure provisioning using **Terraform** and configuration management using **Ansible** on AWS EC2 instances. The goal is to automate the setup of three instances and install a combination of Java, Python, and MySQL across them using role-based playbooks.

📄 **Project PDF**: [Click to view](https://github.com/Vaishnavi-Golhar/Cloud-Resource-Automation-and-Configuration/blob/main/Project%20PDF.pdf)

---

## 🧪 Tasks Performed

### ✅ 1. Setting Up Terraform
- Launched an AWS EC2 instance manually.
- Installed **Terraform** on the same EC2 instance.

### ✅ 2. Provisioning Infrastructure with Terraform
- Created a **Terraform script** to launch **3 EC2 instances** in the **default subnet** (no custom VPCs or subnets).
- Successfully provisioned the infrastructure from the Terraform-installed instance.

### ✅ 3. Ansible Setup
- Installed **Ansible** on the same machine where Terraform is installed.
- Configured passwordless SSH connections from the Ansible master to all 3 newly created EC2 slave instances.

### ✅ 4. Configuration via Ansible Roles
Created three Ansible roles:
- `java`: Installs Java
- `python`: Installs Python
- `mysql`: Installs MySQL

Configured slave nodes as follows:
| Slave | Roles Installed            |
|-------|----------------------------|
| Slave1 | Java + Python             |
| Slave2 | Java + MySQL              |
| Slave3 | MySQL + Python            |

---

## 📂 Files Included

```bash
.
├── terraform/
│   ├── main.tf
│   ├── variables.tf
│   └── output.tf
├── ansible/
│   ├── inventory
│   ├── site.yml
│   └── roles/
│       ├── java/
│       ├── python/
│       └── mysql/
├── README.md
```

---

## 💻 Commands Used

### Terraform
```bash
terraform init
terraform plan
terraform apply
```

### Ansible
```bash
ansible --version
ansible all -m ping
ansible-playbook -i inventory site.yml
```

---

## 👩‍💼 Author

**Vaishnavi Golhar**  
📧 vaishnavigolhar05@gmail.com  
🔗 [LinkedIn](https://www.linkedin.com/in/vaishnavigolhar/)  
📁 GitHub: [Vaishnavi-Golhar](https://github.com/Vaishnavi-Golhar)

