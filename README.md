# wilmardo.ansible-role-oscam

[![Build Status](https://travis-ci.org/wilmardo/ansible-role-oscam.svg?branch=master)](https://travis-ci.org/wilmardo/ansible-role-oscam)
[![Galaxy](https://img.shields.io/badge/galaxy-wilmardo.ansible-role-oscam-blue.svg)](https://galaxy.ansible.com/wilmardo/ansible-role-oscam/)

Role to install oscam

## Requirements

None.

## Role Variables

### Default usage

As default ansible-role-oscam is installed and running.
If you want to adapt this to your needs look at the [Advanced usage](#advanced-usage) section.

### Advanced usage

For more advanced usage the following variables are available:
```yaml
# see defaults/main.yml
```

## Dependencies

None

## Example Playbook

Install ansible-role-oscam with the default settings
```yaml
- hosts: all
  roles:
     - role: wilmardo.ansible-role-oscam
```

## License

BSD-3-Clause-Clear

## Author Information

This role was created in 2018 by [Wilmar den Ouden](https://wilmardenouden.nl).
