# Deploy Wordpress website with ansible

## Description

This is a school project. I've write **Ansible** script to install _Apache_ server with _PHP_ and _mySql_ database, and another script to install a _Wordpress_ website.

## Requirements

You need to have **Ansible** installed on your local host, and **two remote server**, using Linux (write and test for _Ubuntu_, with _Azure_ vms), one for webserver and one for database. Note public and private ips.

## Installation

1. `git clone https://github.com/remi95/Ansible-Wordpress.git`
2. Rename or duplicate all `.dist` files, remove the `.dist` extension, and set your variables. (ansible.cgf and files in group_vars directory)
3. `ansible-playbook install.yml`
4. `ansible-playbook deploy.yml`

## Configuration

:exclamation: Firstly, you need to set your variables.
Edit next files, using parameters on **.dist** files:
- `group_vars/all.yml`
- `group_vars/web/vm.machine1.yml`
- `group_vars/db/vm.machine2.yml`

:grey_exclamation: If you want to send a `dump.sql` file  with your wordpress database, put it on `roles/database/files/<dump_filename>.sql`. Don't forget to set this filename on `group_vars/db/vm.machine1.yml`.
