Role Name
=========

Installs rundeck http://rundeck.org/ role. Also installs Ansible for executing playbooks and etc. Configurable options and Logstash plugin ready.

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

````
---
# defaults file for ansible-rundeck
config_rundeck: true
enable_rundeck: true
enable_rundeck_plugins: true
rundeck_base: /var/lib/rundeck
rundeck_configs:
  - framework.properties
  - rundeck-config.properties
rundeck_db_name: rundeck
rundeck_db_pass: rundeck
rundeck_db_user: rundeck
rundeck_dl_pkg: rundeck-2.5.3-1-GA.deb
rundeck_dl_url: http://dl.bintray.com/rundeck/rundeck-deb/
rundeck_enable_logstash_plugin: false
rundeck_framework_server_hostname: localhost
rundeck_framework_server_name: localhost
rundeck_framework_server_password: admin
rundeck_framework_server_port: 4440
rundeck_framework_server_url: 'http://{{ rundeck_framework_server_hostname }}'
rundeck_framework_server_username: admin
rundeck_framework_ssh_keypath: /var/lib/rundeck/.ssh
rundeck_framework_ssh_keypath_file: '{{ rundeck_framework_ssh_keypath }}/id_rsa'
rundeck_framework_ssh_user: rundeck
rundeck_install_ansible: true
rundeck_logstash_host: []  #defines logstash server if used
rundeck_logstash_port: 9700
rundeck_mysql_backend: false
rundeck_root_dir: /etc/rundeck
````

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: mrlesmithjr.rundeck }

License
-------

BSD

Author Information
------------------

Larry Smith Jr.
- @mrlesmithjr
- http://everythingshouldbevirtual.com
- mrlesmithjr [at] gmail.com
