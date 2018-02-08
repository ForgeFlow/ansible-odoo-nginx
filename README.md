This Ansible role provisions [NGINX][9] with a working configuration for [Odoo][2].

This role takes care of:

- Installing [NGINX][9] using the [NGINX Ansible Role][6]
- Creating a [Odoo][2] specific configuration

## Dependencies

This role depends on the follwoing Ansible Roles:

- [NGINX](https://galaxy.ansible.com/geerlingguy/nginx)

Note: This role uses the [NGINX Ansible Role][6] to ensure the installation
      procedure of [NGINX][9] on the target machnine.

Make sure to include the parameter 'proxy_mode = True' in your odoo
config file.


## Role Variables

Available variables are listed below, along with default values (see
`defaults/main.yml`):

## Example (playbook)

### Basic configuration working on localhost:
```yaml
- name: odoo-nxinx
  hosts: odoo
  roles:
    - ansible-odoo-nginx
```

### Extended configuration
Scenario assuming that you have a domain with specific specific ssl certificates.

```yaml
- name: odoo-nxinx
  hosts: odoo
  roles:
    - ansible-odoo-nginx
  vars:
    - nginx_odoo_server: odoo.mycompany.com
    - ssl_certificate: /etc/letsencrypt/live/odoo.mycompany.com/fullchain.pem
    - ssl_certificate_key: /etc/letsencrypt/live/odoo.mycompany.com/privkey.pem
```
Note: Consider using the ansible-role-certbot [12] in addition to this role, to easily produce valid trusted ssl certificates that you can then refer to as mentioned in the example.


## Variables

See the [defaults/main.yml](defaults/main.yml) file.


## Credits

### Contributors
* Original code from [ridingbytes.ansible-odoo-playbook][11] by [Ridingbytes][1]
* Jordi Ballester Alomar (www.eficent.com)


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
[11]: https://github.com/ridingbytes/ridingbytes.ansible-odoo-playbook "ridingbytes.ansible-odoo-playbook"bytes.ansible-odoo-playbook"
[12]: https://github.com/geerlingguy/ansible-role-certbot
