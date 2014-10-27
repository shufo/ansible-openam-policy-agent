ansible-openam-policy-agent
===========================

A playbook for OpenAM Web Policy Agent for Apache 2.2 on CentOS.

## Overview

It will install Web Policy Agent for Apache 2.2 on CentOS. You can customize it by edit vars file.

## Usage

```bash
ansible-playbook site.yml
```

## vars

```vars/main.yml
apache_conf_dir: /etc/httpd/conf
openam_server_url: 'http://openam.example.com:80/openam'
agent_url: 'http://agent.example.com:80/'
agent_profile_name: test
agent_profile_password: password
```

## Vagrant

You can test on Vagrant virtual machine. (Requires Ansible)

```
vagrant up
```
