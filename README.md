Role Name
=========

Installs rundeck http://rundeck.org/

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

````
config_rundeck: true
enable_firewall: false
enable_logstash_plugin: true
enable_rundeck: true
enable_rundeck_plugins: true
install_ansible: true
mysql_backend: false
rundeck_base: /var/lib/rundeck/libext
rundeck_root: /etc/rundeck
rundeck_db_name: rundeck
rundeck_db_pass: rundeck
rundeck_db_user: rundeck
rundeck_dl_pkg: rundeck-2.5.1-1-GA.deb
rundeck_dl_url: http://dl.bintray.com/rundeck/rundeck-deb/
rundeck_framework_server_name: localhost
rundeck_framework_server_hostname: localhost
rundeck_framework_server_port: 4440
rundeck_framework_server_url: 'http://{{ rundeck_framework_server_hostname }}'
rundeck_framework_server_username: admin
rundeck_framework_server_password: admin
rundeck_framework_ssh_keypath: /var/lib/rundeck/.ssh
rundeck_framework_ssh_keypath_file: '{{ rundeck_framework_ssh_keypath }}/id_rsa'
rundeck_framework_ssh_user: rundeck
rundeck_logstash_host: '{{ logstash_server_fqdn }}'  #defines logstash server if used
rundeck_logstash_port: 9700
````

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

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
