# [mosquitto](#mosquitto)

Install and configure Eclipse Mosquitto

|GitHub|GitLab|Quality|Downloads|Version|Issues|Pull Requests|
|------|------|-------|---------|-------|------|-------------|
|[![github](https://github.com/buluma/ansible-role-mosquitto/workflows/Ansible%20Molecule/badge.svg)](https://github.com/buluma/ansible-role-mosquitto/actions)|[![gitlab](https://gitlab.com/buluma/ansible-role-mosquitto/badges/master/pipeline.svg)](https://gitlab.com/buluma/ansible-role-mosquitto)|[![quality](https://img.shields.io/ansible/quality/59793)](https://galaxy.ansible.com/buluma/mosquitto)|[![downloads](https://img.shields.io/ansible/role/d/59793)](https://galaxy.ansible.com/buluma/mosquitto)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-mosquitto.svg)](https://github.com/buluma/ansible-role-mosquitto/releases/)|[![Issues](https://img.shields.io/github/issues/buluma/ansible-role-mosquitto.svg)](https://github.com/buluma/ansible-role-mosquitto/issues/)|[![PullRequests](https://img.shields.io/github/issues-pr-closed-raw/buluma/ansible-role-mosquitto.svg)](https://github.com/buluma/ansible-role-mosquitto/pulls/)|

## [Example Playbook](#example-playbook)

This example is taken from `molecule/default/converge.yml` and is tested on each push, pull request and release.
```yaml
---
- name: Converge
  hosts: all
  gather_facts: yes
  pre_tasks:
    - name: Install net-tools
      become: yes
      apt:
        name: net-tools
        update_cache: yes
        cache_valid_time: 3600
      when: ansible_os_family == 'Debian'
  tasks:
    - name: "Include buluma.mosquitto"
      ansible.builtin.include_role:
        name: "buluma.mosquitto"
```

The machine needs to be prepared. In CI this is done using `molecule/default/prepare.yml`:
```yaml
---
- name: Prepare
  hosts: all
  gather_facts: no
  become: yes

  roles:
    - role: buluma.bootstrap
```


## [Role Variables](#role-variables)

The default values for the variables are set in `defaults/main.yml`:
```yaml
---
# defaults file for mosquitto
mosquitto_aws_enabled: no
mosquitto_aws_region: eu-west-1
mosquitto_aws_s3_files: []
mosquitto_install_clients: no
mosquitto_limits_nofile_hard: 65535
mosquitto_limits_nofile_soft: 65535
mosquitto_password_file: ~
mosquitto_settings:
  allow_anonymous: yes
  persistence: yes
mosquitto_user_list: {}
mosquitto_version: 1.6.*
```

## [Requirements](#requirements)

- pip packages listed in [requirements.txt](https://github.com/buluma/ansible-role-mosquitto/blob/main/requirements.txt).

## [Status of used roles](#status-of-requirements)

The following roles are used to prepare a system. You can prepare your system in another way.

| Requirement | GitHub | GitLab |
|-------------|--------|--------|
|[buluma.bootstrap](https://galaxy.ansible.com/buluma/bootstrap)|[![Build Status GitHub](https://github.com/buluma/ansible-role-bootstrap/workflows/Ansible%20Molecule/badge.svg)](https://github.com/buluma/ansible-role-bootstrap/actions)|[![Build Status GitLab ](https://gitlab.com/buluma/ansible-role-bootstrap/badges/master/pipeline.svg)](https://gitlab.com/buluma/ansible-role-bootstrap)|

## [Context](#context)

This role is a part of many compatible roles. Have a look at [the documentation of these roles](https://buluma.github.io/) for further information.

Here is an overview of related roles:

![dependencies](https://raw.githubusercontent.com/buluma/ansible-role-mosquitto/png/requirements.png "Dependencies")

## [Compatibility](#compatibility)

This role has been tested on these [container images](https://hub.docker.com/u/buluma):

|container|tags|
|---------|----|
|ubuntu|all|

The minimum version of Ansible required is 2.1, tests have been done to:

- The previous version.
- The current version.
- The development version.



If you find issues, please register them in [GitHub](https://github.com/buluma/ansible-role-mosquitto/issues)

## [Changelog](#changelog)

[Role History](https://github.com/buluma/ansible-role-mosquitto/blob/master/CHANGELOG.md)

## [License](#license)

Apache-2.0

## [Author Information](#author-information)

[buluma](https://buluma.github.io/)
