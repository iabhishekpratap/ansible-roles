# Ansible Role: Web Server Setup

## Overview
This Ansible role sets up and configures a web server using `httpd` on a Linux system. It ensures that the `firewalld` service is properly configured, installs and configures Apache (`httpd`), and applies the necessary configurations.

## Files and Directories

- **fwd-service** - Configures `firewalld` to allow web traffic.
- **httpd-setup** - Sets up and configures the Apache web server (`httpd`).
- **demo.yml** - Example Ansible playbook demonstrating how to use this role.
- **LICENSE** - License file for this project.
- **README.md** - Documentation file.

## Requirements
- Ansible installed on the control machine.
- Target system should support `firewalld` and `httpd`.
- Sudo privileges on the target system.

## Usage
### Running the Role with a Playbook
To apply this role, create a playbook like `demo.yml`:

```yaml
- hosts: web_servers
  become: yes
  roles:
    - ansible-role-webserver
```

Then, execute the playbook with:

```bash
ansible-playbook demo.yml 
```

## Server Web Page
After running the role, the default web page will be available at:

```
http://<server-ip>/
```

To customize the web page, modify the relevant configuration in `httpd-setup`.

## License
This project is licensed under the terms specified in the `LICENSE` file.
