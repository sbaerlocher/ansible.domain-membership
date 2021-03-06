# Ansible Role: domain-membership

[![Build Status](https://img.shields.io/travis/sbaerlocher/ansible.domain-membership.svg?branch=master&style=popout-square)](https://travis-ci.org/sbaerlocher/ansible.domain-membership) [![license](https://img.shields.io/github/license/mashape/apistatus.svg?style=popout-square)](https://sbaerlo.ch/licence) [![Ansible Galaxy](https://img.shields.io/badge/ansible--galaxy-domain--membership-blue.svg?style=popout-square)](https://galaxy.ansible.com/sbaerlocher/domain-membership) [![Ansible Role](https://img.shields.io/ansible/role/d/25073.svg?style=popout-square)](https://galaxy.ansible.com/sbaerlocher/domain-membership)

## Description

Manages the domain membership of a client, which can be a Linux or Windows device.

## Installation

```bash
ansible-galaxy install sbaerlocher.domain-membership
```

## Requirements

This role requires Ansible 2.5 or higher, and platform requirements are listed
in the metadata file.

## Role Variables

| Variable                         | Default | Comments (type) |
| :------------------------------- | :------ | :-------------- |
| domain_membership                | true    |                 |  |
| domain_membership_domain_name    |         |                 |
| domain_membership_admin_user     |         |                 |
| domain_membership_admin_password |         |                 |
| domain_membership_ou             |         |                 |

## Dependencies

For the role to work, the roles [sbaerlocher.domain-join](https://galaxy.ansible.com/sbaerlocher/domain-join) and [sbaerlocher.sssd](https://galaxy.ansible.com/sbaerlocher/sssd) must be installed.

## Example Playbook

```yml
- hosts: all
  roles:
    - sbaerlocher.domain-membership
```

## Changelog

### 1.0.1

- Fixed empty var

### 1.0.0

- initial commit

## Author

- [Simon Bärlocher](https://sbaerlocher.ch)

## License

This project is under the MIT License. See the [LICENSE](https://sbaerlo.ch/licence) file for the full license text.

## Copyright

(c) 2020, Simon Bärlocher
