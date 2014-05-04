Role Name
========

Oracle Jdk ansible role. Completely independent from package manager, so you can use it on any linux distribution. It doesn't require root or sudo permission to run.

Requirements
------------

wget (a no brainer on modern Linux distributions)

Role Variables
--------------

- oracle_jdk_download_dir: download path on the control machine that will be used. Defaults to '/tmp'
- oracle_jdk_package: jdk package name to be downloaded. Defaults to 'jdk-7u51-linux-x64.tar.gz'
- oracle_jdk_version: jdk version name to be instlalled. It will be used to create the instalation file path. Defaults to '1.7.0_51'
- oracle_jdk_instalation_di: instalation prefix that will be used at the hosts. Defaults to '~/jdk'

Dependencies
------------

none

Example Playbook
-------------------------
```
    - hosts: all
      roles:
         - { role: alexanderjardim.oracle_jdk }
```
License
-------

BSD

Author Information
------------------

alexander.ramos.jardim+oracle_jdk@gmail.com
