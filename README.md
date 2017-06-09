ansible-java8-oracle
====================

Ansible role to install the Oracle Java8.

Should work on Ubuntu, Mint, CentOS 7. Debian has no ppa suport AFAIK.

Licence is auto-accepted (no prompt) and the whole thing is idempotent
(executing it several times will not do unneeded steps again).

(Almost) no usage of 'shell:', only ansible commands.


Requirements
------------
None.

Role Variables
--------------
Optional variables:
- rpm_package_name (CentOS 7 only), Java package name to install (default is "jdk1.8.0_131");
- rpm_package_url (CentOS 7 only), URL of Java package to install (default is oracle.com link for "jdk1.8.0_131" package).

Dependencies
------------
None.

Example Playbook
----------------
```yaml
    - hosts: servers
      roles:
        - ansible-java8-oracle
          rpm_package_name: jdk1.8.0_131
          rpm_package_url: http://download.oracle.com/otn-pub/java/jdk/8u131-b11/d54c1d3a095b4ff2b6607d096fa80163/jdk-8u131-linux-x64.rpm
```

License
-------
GPL V3, but that is interesting on fork only, you can use it at will.
