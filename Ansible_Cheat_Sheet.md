# Ansible Cheat Sheet
## Ansible Architecture
![image](https://github.com/imansadegh/Ansible/assets/36385769/9fedc4b4-a632-4099-9e2d-3a7d27e12ddc)

## How Ansible Works
![image](https://github.com/imansadegh/Ansible/assets/36385769/31435410-60b0-41e2-b54a-7c0e88fec86a)

## Inistallation
1. In the first we install epel-release after that we need to install python2 and python3.<br>
2. 
```
yum/apt install ansible<br>
```
3. install ssh-keygen on controller and servers<br>
4. vim ansible.cfg and change this in below to have permission to change root user when you write sudo su<br>

```
[privilege_escalation]<br>
become=true<br>
become_method=sudo<br>
become_user=root<br>
become_ask_pass=false<br>
```

## Directories
1. config file: /etc/ansible/ansible.cfg<br>
2. modules directory: /usr/lib/python2.7/site-packages/ansible/modules<br>
 
## Commands
### ad-hoc
```ànsible -i [invenotry file] -m [modules] -a [module argument]```<br>

with this command you use ping module to check connection between controller and other servers:<br>

```
ansible group_name_on_host_file_in_inventory -m ping 
```
