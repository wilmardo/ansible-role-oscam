# wilmardo.ansible-role-oscam

[![Build Status](https://travis-ci.org/wilmardo/ansible-role-oscam.svg?branch=master)](https://travis-ci.org/wilmardo/ansible-role-oscam)
[![Galaxy](https://img.shields.io/badge/galaxy-wilmardo.ansible-role-oscam-blue.svg)](https://galaxy.ansible.com/wilmardo/ansible-role-oscam/)

Role to install the OSCam softcam.

## Requirements

None.

## Role Variables

### Default usage

As default ansible-role-oscam is installed and running.
If you want to adapt this to your needs look at the [Advanced usage](#advanced-usage) section.

### Advanced usage

For more advanced usage the following variables are available:
```yaml
# Choose the package to install, oscam for latest or oscam-svn for trunk
oscam_version: oscam-svn

# The oscam.conf in YAML format. Each section has its own nested dict like this:
# [global]  >     global:
# nice = 1  >     nice: 1
oscam_conf:
  global:
    nice: -1
    WaitForCards: 1

  newcamd:
    key: 000102030405060708090A0B0C0D
    port: 25001@0606:047371

# The oscam.server in YAML format
oscam_server:
  reader:
    label: CAIW
    device: /dev/ttyUSB0
    mhz: 600
    cardmhz: 600
    detect: cd
    protocol: mouse
    group: 1
    caid: 0606
    rsakey: "3C8633AAC0D367533DEC7BB2EEEDEB8CA3ADA52E58B99BB34672783277A1DAAC3B610\
            6AD0909774E031B2A6E30195B437683AD0FC599B87D08CEA47BE1B6C76A"
    boxkey: 1122334455667788
    chid: 0606:000005,000001,000018,007FFE,007FFD,00FDD8
    emmcache: 1,3,2
    auprovid: 047371

# The oscam.user in YAML format
oscam_user:
  account:
    user: oscam
    pwd: password
    group: 1
    au: CAIW
    caid: 0606
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
