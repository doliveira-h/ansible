# Ansible Playbooks
This project is a collection of playbooks used for tests purposes


### Tech

Playbooks/Roles description:

* [deploy-zabbix-agent] - Install and configure zabbix agent version 3.4.2
* [openshift-prereqs] - Install and configure pre-requisites packages and files to install Openshift 3.9
* [os-master-cfg] - Maintain and enforce Openshift Master and Docker configuration (will be used with AWX/Tower)


### Installation

Install Ansible:

* Ubuntu
```sh
$ sudo apt update
$ sudo apt install software-properties-common
$ sudo apt-add-repository --yes --update ppa:ansible/ansible
$ sudo apt install ansible
```

* Centos 7
```sh
$ sudo yum install epel-release
$ sudo yum install ansible
```

### Running Playbooks

Inventory sample:

```sh
[vars:all]
ansible_user=ansible

[servers]
server01
server02
192.168.1.100
```

Run a playbook:
```sh
$ ansible-playbook -i <path to inventory file> <playbook_name>
```