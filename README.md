openssh
=======

Installs and configures OpenSSH.

Requirements
------------

This role requires Ansible 1.4 or higher.

Role Variables
--------------

    # List of OpenSSH packages (Needs to be modified at distribution level)
    openssh_packages: []
    # Name of the OpenSSH service
    openssh_service_name: sshd

    # Path and filename of OpenSSH server configuration file
    openssh_server_config_file: /etc/ssh/sshd_config
    # Owner of OpenSSH server configuration file
    openssh_server_config_file_owner: root
    # Group of OpenSSH server configuration file
    openssh_server_config_file_group: root
    # Permissions of OpenSSH server configuration file
    openssh_server_config_file_mode: "0600"

    # Path and filename of OpenSSH client configuration file
    openssh_client_config_file: /etc/ssh/ssh_config
    # Owner of OpenSSH client configuration file
    openssh_client_config_file_owner: root
    # Group of OpenSSH client configuration file
    openssh_client_config_file_group: root
    # Permissions of OpenSSH client configuration file
    openssh_client_config_file_mode: "0644"

Dependencies
------------

Example Playbook
----------------

1) Installs OpenSSH with default settings.

    - hosts: all
      roles:
         - { role: openssh }

License
-------

BSD

Author Information
------------------

Kevin Brebanov
