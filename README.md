Oracle JDK
=========

This role downloads and installs an Oracle JDK and sets it up as the default JDK on Ubuntu. The download is cached in a local directory on the machine running Ansible and synchronized to remote hosts. This saves time and bandwidth.

[![Build Status](https://travis-ci.org/Rheinwerk/ansible-role-oracle_jdk.svg?branch=master)](https://travis-ci.org/Rheinwerk/ansible-role-oracle_jdk)

Requirements
------------

None.

Role Variables
--------------

There are two variables that drive this role: `_jdk` and `RW_APT_CACHE_UPDATE`. `_jdk` is a map that contains all configuration and settings for this role. `RW_APT_CACHE_UPDATE` may be specified as _extra variables_ when invoking Ansible in order to force `apt-get update`. Please see `defaults/main.yml` for details.

Dependencies
------------

None.

Example Playbook
----------------

The general contract of this role is to take the variables map `_jdk` from `defaults/main.yml` as a template for your configuration and pass that configuration as a parameter to this role.

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      var:
        JDK:
          ...
      roles:
         - { role: oracle_jdk, tags: [ 'jdk' ], _jdk: "{{ JDK }}" }

License
-------

Please see LICENSE.

Author Information
------------------

Original author is [Daniel Schneller](https://github.com/dschneller) as member of the [Rheinwerk](https://github.com/Rheinwerk) project.

