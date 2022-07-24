# [mosquitto](#mosquitto)

Install and configure Eclipse Mosquitto

|GitHub|GitLab|Quality|Downloads|Version|Issues|Pull Requests|
|------|------|-------|---------|-------|------|-------------|
|[![github](https://github.com/buluma/ansible-role-mosquitto/workflows/Ansible%20Molecule/badge.svg)](https://github.com/buluma/ansible-role-mosquitto/actions)|[![gitlab](https://gitlab.com/buluma/ansible-role-mosquitto/badges/master/pipeline.svg)](https://gitlab.com/buluma/ansible-role-mosquitto)|[![quality](https://img.shields.io/ansible/quality/)](https://galaxy.ansible.com/buluma/mosquitto)|[![downloads](https://img.shields.io/ansible/role/d/)](https://galaxy.ansible.com/buluma/mosquitto)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-mosquitto.svg)](https://github.com/buluma/ansible-role-mosquitto/releases/)|[![Issues](https://img.shields.io/github/issues/buluma/ansible-role-mosquitto.svg)](https://github.com/buluma/ansible-role-mosquitto/issues/)|[![PullRequests](https://img.shields.io/github/issues-pr-closed-raw/buluma/ansible-role-mosquitto.svg)](https://github.com/buluma/ansible-role-mosquitto/pulls/)|

## [Example Playbook](#example-playbook)

This example is taken from `molecule/default/converge.yml` and is tested on each push, pull request and release.
```yaml
---
- name: Converge
  hosts: all
  tasks:
    - name: "Include buluma.mosquitto"
      ansible.builtin.include_role:
        name: "buluma.mosquitto"
```


## [Role Variables](#role-variables)

The default values for the variables are set in `defaults/main.yml`:
```yaml
---
# defaults file for mosquitto
```

## [Requirements](#requirements)

- pip packages listed in [requirements.txt](https://github.com/buluma/ansible-role-mosquitto/blob/main/requirements.txt).


## [Context](#context)

This role is a part of many compatible roles. Have a look at [the documentation of these roles](https://buluma.github.io/) for further information.

Here is an overview of related roles:

![dependencies](https://raw.githubusercontent.com/buluma/ansible-role-mosquitto/png/requirements.png "Dependencies")

## [Compatibility](#compatibility)

This role has been tested on these [container images](https://hub.docker.com/u/buluma):

|container|tags|
|---------|----|
|fedora|all|
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
