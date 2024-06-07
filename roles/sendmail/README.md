sendmail
=========
```
Sends a mail
```
Requirements
------------

Role Variables
--------------
```
smtpserver: smtp.office365.com
smtp_port: 587
smtp_username: mickey.mouse@exmaple.com
smtp_password: 123456
my_server: null
mailfrom: mickey.mouse@exmaple.com (Mickey Mouse)
mailto:
- Mickey Mouse <mickey.mouse@exmaple.com>
- Donald Duck <donald.duck@example.com>
bccto:
- Mickey Mouse <mickey.mouse@exmaple.com>
- Donald Duck <donald.duck@example.com>
```
Dependencies
------------

Example Playbook
----------------
```
---
- name: Sends a mail
  hosts: localhost
  connection: local

  roles:

    - role: sendmail
```
License
-------

https://opensource.org/license/mit
