Role Name
=========

A brief description of the role goes here.

Requirements
------------

The Role assumes that the redhat/centos repositories are in place and enabled.Works on redhat based systems.

Role Variables
--------------

packages:
  - bind
  - bind-utils
network: '192.168.122.0/24'
service: named
domain: example.com
user: root
dummy: node11
dummy_ip: 10.0.0.1


Packages: The default dns package(bind) and some tools(bind-utils)
network:  your network that's allowed to query the dns server
service:  name of the dns service (named in redhat based systems)
user:     the default user to whom emails should go
dummy:    dummy host
dummy_ip: dummy ip for the "dummy" host. 

Dependencies
------------

No dependencies.

Example Playbook
----------------

The role is called with the simplest of forms.

---
- hosts: node2
  roles:
  - dns


License
-------

BSD

Author Information
------------------

Author: Ashish Nair
email: ashish882000@yahoo.co.in
