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
# Agent User Response File
CONFIG_DIR= /etc/httpd/conf
AM_SERVER_URL= http://openam-proxy-test.example.com:80/openam
AGENT_URL= http://agent-test.example.com:80/
AGENT_PROFILE_NAME= test
AGENT_PASSWORD_FILE= /tmp/openam_agent_pwd.txt
```
