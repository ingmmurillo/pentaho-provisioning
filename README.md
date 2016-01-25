# Provisioning Pentaho BI Server CE v5.4 and PostgreSQL v9.4 on CentOS v7
The following code automates the procedure to install and configure base software ([**Java 7**](http://www.oracle.com/technetwork/java/javase/downloads/index.html)),  [**Pentaho BI Server v5.4**](http://sourceforge.net/projects/pentaho/files/Business%20Intelligence%20Server/5.4/) and [**PostgreSQL**](http://www.postgresql.org/download/) on an operating system CentOS v7.

This **IAC** (Infrastructure as Code) allows you to have *Pentaho BI Server v5.4* configured on *PostgreSQL* repositories: (**hibernate**, **quartz**, **jackrabbit**) with only one command.

Before using this code, make sure you have installed the following:
* [**Ansible**](http://docs.ansible.com/ansible/intro_installation.html)
* [**Vagrant**](https://www.vagrantup.com/docs/installation/)
* [**VirtualBox**](https://www.virtualbox.org/)

To run the provisioning code, open a terminal console and run:
```sh-session
vagrant up
```
To test that you have successfully provisioned **Pentaho CE**, open a browser an hit the following URL:
```sh-session
http://localhost:8888/pentaho/
```

**NOTES:**
* Just the first time you run the command, it will take some minutes
* [**Ansible**](http://www.ansible.com/) and [**Vagrant**](http://www.vagrantup.com/) runs well on Linux distributions and OS X. To run those on Windows is tricky, but not impossible!
* This code automates all the procedures mentioned in my [**blog post**](https://translate.google.com/translate?hl=en&sl=auto&tl=en&u=http%3A%2F%2Fingmmurillo-dwh-bi.blogspot.com%2F2014%2F10%2Fconfiguracion-de-pentaho-bi-server-52.html)
