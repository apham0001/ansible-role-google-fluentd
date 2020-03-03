Role Name
=========

Install Google-fluentd

Requirements
------------

The Google Cloud monitoring API must be enabled.

Role Variables
--------------

### Apache
By default the role change apache.conf to be compliant with default Debian log name

### PHP
add 2 configurations in php.conf to manage slow and error logs
Each vhost are defined in ```google_fluentd_php_log_names```

```
vars:
  google_fluentd_php:
    - website1
    - website2
```

Example Playbook
----------------

vars:
  google_fluentd_php_log_names:
    - website1

roles:
  - apham0001.google-fluentd

License
-------

BSD / MIT
