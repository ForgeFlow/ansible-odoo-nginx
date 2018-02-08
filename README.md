
# RIDING BYTES: NGINX Role

This role provisions [NGINX][9] with a working configuration for [Odoo][2].

This role takes care of:

- Installing [NGINX][9] using the [NGINX Ansible Role][6]
- Creating a [Odoo][2] specific configuration



## Dependencies

This role depends on the follwoing Ansible Roles:

- [NGINX](https://galaxy.ansible.com/geerlingguy/nginx)

Note: This role uses the [NGINX Ansible Role][6] to ensure the installation
      procedure of [NGINX][9] on the target machnine.

## Role Variables

Available variables are listed below, along with default values (see
`defaults/main.yml`):

## Thanks to
Original code from ridingbytes_nginx by [Ridingbytes_nginx][1]


[1]:  http://ridingbytes.com "RIDING BYTES"
[2]:  https://odoo.com "Odoo ERP"
[3]:  https://www.vagrantup.com/docs/getting-started/ "Vagrant"
[4]:  https://www.ansible.com "Ansible"
[5]:  https://docs.ansible.com/ansible/playbooks.html "Ansible Playbook"
[6]:  https://docs.ansible.com/ansible/playbooks_roles.html "Ansible Roles"
[7]:  https://galaxy.ansible.com "Ansible Galaxy"
[8]:  https://docs.ansible.com/ansible/intro_inventory.html "Ansible Inventory"
[9]:  http://www.nginx.org "NGINX"
[10]: https://galaxy.ansible.com/geerlingguy/nginx "NGINX Ansible Role"
