# ansible-elastic-centos

ansible role to install Elastic Products on CentOS from official repositories for YUM

https://galaxy.ansible.com/suzuki-shunsuke/elastic-centos/

Requirements
------------

Nothing.

Role Variables
--------------

* elastic_name: elastic product's name.
  * elasticsearch
  * kibana
  * logstash
  * filebeat
  * etc
* elastic_state(optional): elastic service state.
* elastic_version(optional): elastic version.
* elastic_enabled(optional): whether elastic service is enabled.

Dependencies
------------

Nothing.

Example Playbook
----------------

```yaml
- hosts: servers
  roles:
  - role: suzuki-shunsuke.elastic-centos
    elastic_name: elasticsearch
    elastic_state: started
    elastic_enabled: yes
    elastic_version: 5.4.0
```

License
-------

[MIT](LICENSE)
