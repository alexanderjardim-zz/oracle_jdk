Role Name
========

Oracle Jdk ansible role. Completely independent from package manager, so you can use it on any linux distribution. It doesn't require root or sudo permission to run.

All my roles make the assumption that host machines don't have internet connection, as this is the standard behavior of production machines in most companies. So, all the necessary dependencies will be downloaded to the control machine and after that pushed to the host machines. Keep in mind that you will need disk space for these downloads on your control machine.

Requirements
------------

wget (a no brainer on modern Linux distributions)

Role Variables
--------------

- oracle_jdk_download_dir: download path on the control machine that will be used. Defaults to '/tmp'
- oracle_jdk_package: jdk package name to be downloaded. Defaults to 'jdk-7u51-linux-x64.tar.gz'
- oracle_jdk_version: jdk version name to be instlalled. It will be used to create the instalation file path. Defaults to '1.7.0_51'
- oracle_jdk_instalation_dir: instalation prefix that will be used at the hosts. Defaults to '/home/vagrant/jdk'

Dependencies
------------

none

Example Playbook
-------------------------
```
    - hosts: all
      roles:
         - { role: alexanderjardim.oracle_jdk, oracle_jdk_instalation_dir: '/your/jvm/path' }
```
License
-------

BSD

Author Information
------------------

alexander.ramos.jardim+oracle_jdk@gmail.com
