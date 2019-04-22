# Deploy Wordpress website with ansible

## Description

This is a school project. I've write **Ansible** script to install _Apache_ server with _PHP_ and _mySql_ database, and another script to install a _Wordpress_ website.

## Installation

1. `git clone https://github.com/remi95/Ansible-Wordpress.git`
2. Rename or duplicate all `.dist` files, remove the `.dist` extension, and set your variables. (ansible.cgf and files in group_vars directory)
3. `ansible-playbook install.yml`
4. `ansible-playbook deploy.yml`

## Configuration

Set your servers ips in `group_vars/db/vm.machine2.yml` and `group_vars/web/vm.machine1.yml`, after the `ansible_host` key.

All database configurations are in `group_vars/all.yml` file.

If you want to send a `dump.sql` file to import your database during the deployment, put it on `roles/database/files`, and set the filename after the `dump_filename` key of the _db vars file_.
