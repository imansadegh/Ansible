# Ansible Repository

![Ansible Logo](https://www.ansible.com/hubfs/2016_Images/Assets/Ansible-Mark-Large-RGB-Pool.png)

Welcome to my Ansible repository! This repository contains a collection of Ansible playbooks and roles that I've created to automate various tasks, including server setup, configuration, and application deployment. Below, you'll find a brief overview of the contents of this repository.

## Contents

### 1. Playbooks

- [Install Zabbix](playbooks/zabbix_installation.yml): An Ansible playbook to install Zabbix server and agents on specified hosts, along with necessary configurations.

### 2. Roles

- [MySQL Role](roles/zabbix/mysql): A role to install and configure MySQL server.

- [PHP Role](roles/zabbix/php): A role to install PHP and required PHP modules.

### 3. Inventory

- [hosts.yml](inventory/hosts.yml): The inventory file that defines the target hosts for the playbooks. Adjust this file to include your own server details.

## How to Use

1. Clone the repository to your local machine:

   ```bash
   git clone https://github.com/civiliman/ansible.git
   cd ansible
Ensure you have Ansible installed on your local machine. If not, follow the official Ansible installation guide.

Update the inventory file (inventory/hosts.yml) with your target server details.

Run the desired playbook using the ansible-playbook command. For example, to install Zabbix:

bash
Copy code
ansible-playbook playbooks/zabbix_installation.yml
Enjoy the automation! Sit back and relax while Ansible takes care of the server setup and configuration.

Contribution
I welcome contributions to this repository! If you have improvements, bug fixes, or new ideas for playbooks and roles, feel free to create a pull request. Let's make this Ansible repository even more powerful together!

Disclaimer
These playbooks are provided as-is and without any warranty. Always test them in a controlled environment before using them in production.

License
This repository is licensed under the MIT License. Feel free to use, modify, and distribute the code as per the terms of the license.

Happy automating with Ansible! If you have any questions, feel free to open an issue in this repository.

Iman Sadegh
