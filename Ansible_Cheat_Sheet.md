# Ansible Cheat Sheet
## Ansible Architecture
![image](https://github.com/imansadegh/Ansible/assets/36385769/9fedc4b4-a632-4099-9e2d-3a7d27e12ddc)

## How Ansible Works
![image](https://github.com/imansadegh/Ansible/assets/36385769/31435410-60b0-41e2-b54a-7c0e88fec86a)

## Inistallation
1. In the first we install epel-release after that we need to install python2 and python3.<br>
2. 
```
yum/apt install ansible
```
3. install ssh-keygen on controller and servers<br>
4. vim ansible.cfg and change this in below to have permission to change root user when you write sudo su<br>

```
[privilege_escalation]
become=true
become_method=sudo
become_user=root
become_ask_pass=false
```

## Directories
1. config file: /etc/ansible/ansible.cfg<br>
2. modules directory: /usr/lib/python2.7/site-packages/ansible/modules<br>
 
## Commands
### ad-hoc
```ansible -i [invenotry file] -m [modules] -a [module argument]```<br>

with this command you use ping module to check connection between controller and other servers:<br>

```
ansible group_name_on_host_file_in_inventory -m ping 
```
for example :
```
ansible 192.168.22.214 -m ping
ansible all -m copy -a 'src=home/user1/ansible/file1 dest=/home'
ansible 192.168.22.214 -m copy -a 'dest=/home/file1 content="hi" mode=0755''
ansible 192.168.22.214 -m file -a 'path=/home/file1 state=absent'
```
In the first line command you can see all of module in ansible and with the second command you can read about specific module that you want:
```
ansible-doc -l
ansible-doc module_name
```
or you can use ansible site:
https://docs.ansible.com

with this command you use setup module for gathering datas:
'''
ansible 192.168.22.214 -m setup -a 'filter=ansible_kernel'
'''

