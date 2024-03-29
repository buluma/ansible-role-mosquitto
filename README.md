# Ansible role [mosquitto](https://galaxy.ansible.com/ui/standalone/roles/buluma/mosquitto/documentation)

Install and configure Eclipse Mosquitto

|GitHub|Version|Issues|Pull Requests|Downloads|
|------|-------|------|-------------|---------|
|[![github](https://github.com/buluma/ansible-role-mosquitto/actions/workflows/molecule.yml/badge.svg)](https://github.com/buluma/ansible-role-mosquitto/actions/workflows/molecule.yml)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-mosquitto.svg)](https://github.com/buluma/ansible-role-mosquitto/releases/)|[![Issues](https://img.shields.io/github/issues/buluma/ansible-role-mosquitto.svg)](https://github.com/buluma/ansible-role-mosquitto/issues/)|[![PullRequests](https://img.shields.io/github/issues-pr-closed-raw/buluma/ansible-role-mosquitto.svg)](https://github.com/buluma/ansible-role-mosquitto/pulls/)|[![Ansible Role](https://img.shields.io/ansible/role/d/buluma/mosquitto)](https://galaxy.ansible.com/ui/standalone/roles/buluma/mosquitto/documentation)|

## [Example Playbook](#example-playbook)

This example is taken from [`molecule/default/converge.yml`](https://github.com/buluma/ansible-role-mosquitto/blob/master/molecule/default/converge.yml) and is tested on each push, pull request and release.

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

The machine needs to be prepared. In CI this is done using [`molecule/default/prepare.yml`](https://github.com/buluma/ansible-role-mosquitto/blob/master/molecule/default/prepare.yml):

```yaml
---
- name: Prepare
  hosts: all
  gather_facts: no
  become: yes

  roles:
    - role: buluma.bootstrap
```

Also see a [full explanation and example](https://buluma.github.io/how-to-use-these-roles.html) on how to use these roles.

## [Role Variables](#role-variables)

The default values for the variables are set in [`defaults/main.yml`](https://github.com/buluma/ansible-role-mosquitto/blob/master/defaults/main.yml):

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

- pip packages listed in [requirements.txt](https://github.com/buluma/ansible-role-mosquitto/blob/master/requirements.txt).

## [State of used roles](#state-of-used-roles)

The following roles are used to prepare a system. You can prepare your system in another way.

| Requirement | GitHub | Version |
|-------------|--------|--------|
|[buluma.bootstrap](https://galaxy.ansible.com/buluma/bootstrap)|[![Ansible Molecule](https://github.com/buluma/ansible-role-bootstrap/actions/workflows/molecule.yml/badge.svg)](https://github.com/buluma/ansible-role-bootstrap/actions/workflows/molecule.yml)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-bootstrap.svg)](https://github.com/shadowwalker/ansible-role-bootstrap)|

## [Context](#context)

This role is a part of many compatible roles. Have a look at [the documentation of these roles](https://buluma.github.io/) for further information.

Here is an overview of related roles:

![dependencies](https://raw.githubusercontent.com/buluma/ansible-role-mosquitto/png/requirements.png "Dependencies")

## [Compatibility](#compatibility)

This role has been tested on these [container images](https://hub.docker.com/u/buluma):

|container|tags|
|---------|----|
|[Ubuntu](https://hub.docker.com/repository/docker/buluma/ubuntu/general)|all|

The minimum version of Ansible required is 2.1, tests have been done to:

- The previous version.
- The current version.
- The development version.

If you find issues, please register them in [GitHub](https://github.com/buluma/ansible-role-mosquitto/issues)

## [Changelog](#changelog)

[Role History](https://github.com/buluma/ansible-role-mosquitto/blob/master/CHANGELOG.md)

## [License](#license)

[Apache-2.0](https://github.com/buluma/ansible-role-mosquitto/blob/master/LICENSE)

## [Author Information](#author-information)

[Shadow Walker](https://buluma.github.io/)

