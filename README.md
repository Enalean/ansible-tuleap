Role Name
=========

Manage installation and update of a tuleap server.

Requirements
------------

A RHEL >=7.5 server

Main Variables
--------------

    - tuleap_fqdn:           The domain name you will use to access tuleap like tuleap.example.com (default: the server ip address)
    - tuleap_admin_email:    The admin email of the tuleap platform
    - tuleap_packages:       Main tuleap packages and a list of common plugins to install
    - tuleap_packages_state: Can be present or latest. Default is present (no update)

Dependencies
------------

    - None

Example Playbook
----------------

    - hosts: tuleap
      roles:
         - role: ansible-tuleap
      vars:
         tuleap_fqdn:           tuleap.example.com
         tuleap_admin_email:    admin@tuleap.example.com
         tuleap_packages_state: latest

License
-------

BSD

Author Information
------------------

    - [Tuleap](https://www.tuleap.org)
    - [Enalean](https://www.enalean.com)
    - [Community](tuleap.net)
    - [Community Chat](chat.tuleap.org)
