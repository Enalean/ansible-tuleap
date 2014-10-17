Role Name
=========

Manage installation and update of a tuleap server.

Requirements
------------

A RHEL >=6.5 server

Role Variables
--------------

    - tuleap_version:  Can be stable or master, debian will eventually come (default: master)
    - tuleap_domain:   The domain name you will use to access tuleap like tuleap.example.com (default: the server ip address)
    - tuleap_org_name: Your company name (default: Tuleap)

Dependencies
------------

    - goozbach.EPEL (but will be changed cause i'm not satisfied)
    - more to come

Example Playbook
----------------

    - hosts: tuleap
      roles:
         - { role: enalean.ansible-tuleap, tuleap_version=master, tuleap_domain=tuleap.net }

License
-------

BEER-WARE

Author Information
------------------

    - Author: Thomas Cottier (thomas.cottier+ansible@enalean.com)
    - Product: Tuleap (www.tuleap.org)
    - Company: Enalean (www.enalean.com)
