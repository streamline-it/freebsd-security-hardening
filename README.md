Role Name
=========

freebsd-security-hardening

This roles will secure a FreeBSD host.  Currently is secures the following:

	fork bomb mitigation.  Changes the values to maxproc under /etc/login.conf

Requirements
------------

None

Role Variables
--------------

Defaults:

# Limits maximum processes for regular user accounts
# This will limit damage a forkbomb can do on a host
freebsd_security_hardening_maxproc: 300

Vars:

#Path to the login.conf file
freebsd_security_hardening_login_cfg_filepath: /etc/login.conf

Dependencies
------------

None.

Example Playbook
----------------

- name: Example use of freebsd-security-hardening role
  hosts: servers
  become: true

  roles:
     - name: freebsd-security-hardening


License
-------

BSD

Author Information
------------------

Rich O'Hara

