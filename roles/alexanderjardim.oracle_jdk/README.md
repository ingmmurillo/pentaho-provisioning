oracle_jdk
========

Oracle Jdk ansible role. Completely independent from package manager, so you can use it on any linux distribution. It doesn't require root or sudo permission to run.

You must keep in my mind three things when you use my roles:

1. All my roles make the assumption that host machines don't have internet connection, as this is the standard behavior of production machines in most companies. So, all the necessary dependencies will be downloaded to the control machine and after that pushed to the host machines. Keep in mind that you will need disk space for these downloads on your control machine.
1. I try to not use any package manager, at all. This way, you will not depend on more than one maintainer for the same software (the software original writer, and the package management team). Going this way, it is your choice to install using root or not. Which I always advise to don't use, if you can.
1. I try to keep all of my roles free from sudo or root access. If you want to use root, it is by choice and not a specific requirement. I will keep it this way as long as I can.


Requirements
------------

wget (a no brainer on modern Linux distributions)

Role Variables
--------------

- **oracle_jdk_download_dir**: download path on the control machine that will be used. Defaults to *'/tmp'*
- **oracle_jdk_package**: jdk package name to be downloaded. Defaults to *'jdk-7u60-linux-x64.tar.gz'*
- **oracle_jdk_package_subdir**: sub-directory for Oracle otn-pub folder. Related to jdk_package. Defaults to *'7u60-b19'*
- **oracle_jdk_version**: jdk version name to be installed. It will be used to create the installation file path. Defaults to *'1.7.0_60'*
- **oracle_jdk_installation_dir**: installation prefix that will be used at the hosts. Defaults to *'/home/vagrant/jdk'*

Dependencies
------------

none

Example Playbook
-------------------------
```
    - hosts: all
      roles:
         - { role: alexanderjardim.oracle_jdk, oracle_jdk_installation_dir: '/your/jvm/path' }
```
License
-------

BSD

Author Information
------------------

alexander.ramos.jardim+oracle_jdk@gmail.com
