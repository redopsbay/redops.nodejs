# redops.nodejs #

RedOps NodeJS Provisioning using NodeJS Version Manager (NVM)

Role Variables
--------------
 - domain_name (Domain Name System) of the target website
 - node_version (NodeJS Version to be used)
 - server_alias ( used for www.domain.com )
 - service_port (NodeJS Listen Port for NGINX Reverse Proxy)
 - node_packages (NodeJS Packages to be installed optionally)
 - unix_user ( Unix Username )

Example Playbook
----------------
Example Playbook for lamp stack provisioning:

    - hosts: vagrant
      gather_facts: yes
      become: yes
      vars:
        domain_name: domain.com
        server_alias: www.domain.com
        service_port: 3000
        unix_user: ubuntu
        node_version: v12.20.2
        node_packages: react
      roles:
      - hive.nodejs
      ignore_errors: '{{ ansible_check_mode }}'

      
License
-------

BSD

Author Information
------------------

Name: Alfred Valderrama
Email: alfred98valderrama@gmail.com
Github Repository: https://github.com/alfredvalderrama98
Website: https://goadminops.com
