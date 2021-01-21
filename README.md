# SimpleSAMLphp-Ansible
Ansible script for SimpleSAMLphp


contact: remko@whay.nl


# Example Playbook

---
# Title: srv-saml-01
#
# Author: Remko van den Hoef
# File: samlserverpb.yml
#
# Description:
#   Playbook SimpleSAMLphp

- hosts: servername
  become: yes

  vars:
    servername  : 'saml.example.com'
    baseurl     : 'saml.example.com'
    authadmin   : 'Password123'
    secretsalt  : '12345678901234567890123456789012'
    contactmail : 'email@example.com'
    timezone    : 'Europe/Amsterdam'

  roles:
    - SimpleSAMLphp-Ansible
