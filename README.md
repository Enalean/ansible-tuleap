Role Name
=========

Manage installation and update of a tuleap server.

Requirements
------------

A RHEL >=6.5 server

Warning
-------

This role default is to install tuleap-plugin-git-gitolite3 package which is not compatible with older versions of tuleap-plugin-git. If you are not running a new installation and want to update your tuleap packages, check which version is installed and tweak the tuleap_packages variable.

Role Variables
--------------

    - tuleap_version:        Can be stable or master, debian will eventually come (default: master)
    - tuleap_domain:         The domain name you will use to access tuleap like tuleap.example.com (default: the server ip address)
    - tuleap_org_name:       Your company name (default: Tuleap)
    - tuleap_packages:       Main tuleap packages and a list of common plugins to install
    - tuleap_packages_state: Can be present or latest. Default is present (no update)

Dependencies
------------

    - None

Example Playbook
----------------

    - hosts: tuleap
      roles:
         - { role: enalean.ansible-tuleap, tuleap_version=master, tuleap_domain=tuleap.example.com, tuleap_packages_state=latest }

License
-------

BSD

Author Information
------------------

    - Author: Thomas Cottier (thomas.cottier+ansible@enalean.com)
    - Product: Tuleap (www.tuleap.org)
    - Company: Enalean (www.enalean.com)
