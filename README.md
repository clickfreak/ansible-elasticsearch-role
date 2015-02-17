Ansible Elastisearch Role
=========================

This role installs and configures Elasticsearch from official deb repository.

Features
--------
- install elasticsearch with openjdk-7-jre-headless
- install elasticsearch plugins (variable elasticsearch_plugins, by default install karmi/elasticsearch-paramedic)
- full elasticsearch configuration over role variable (variable elasticsearch_config)

Examples
========

```
- name: deploy elasticsearch server
  hosts: elasticsearch
  sudo: yes

  roles:
    - role: clickfreak.elasticsearch
      elasticsearch_version: 1.4
      elasticsearch_config:
        network.bind_host: 127.0.0.1
        network.host: 127.0.0.1
        network.publish_host: 127.0.0.1
        http.bind_host: 127.0.0.1
        http.host: 127.0.0.1
        http.publish_host: 127.0.0.1
      elasticsearch_plugins:
      	- karmi/elasticsearch-paramedic

```

Author Information
------------------

Konstantin Novakovsky / Selectel LLC
