# ansible-elastic-centos

ansible role to install Elastic Products on CentOS from official repositories for YUM

https://galaxy.ansible.com/suzuki-shunsuke/elastic-centos/

## Requirements

Nothing.

## Role Variables

name | required | default | example | description
--- | --- | --- | --- | ---
elastic_name | yes | | kibana | elastic product's name
elastic_state | no | | started | elastic service state
elastic_version | no | | 5.3.0 | elastic version
elastic_enabled | no | | | whether elastic service is enabled
elastic_java | no | java is not installed | java-1.8.0-openjdk | yum package name to install java

## Dependencies

Nothing.

## Example Playbook

```yaml
- hosts: servers
  roles:
  - role: suzuki-shunsuke.elastic-centos
    elastic_name: elasticsearch
    elastic_state: started
    elastic_enabled: yes
    elastic_version: 5.4.0
    elastic_java: java-1.8.0-openjdk
    become: yes
```

## License

[MIT](LICENSE)
