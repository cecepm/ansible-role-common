# Ansible Role Ubuntu Common

Bootstrap Ubuntu server. This is 'meta' roles. All task included from other roles.

By default this ansible role, will configure

- Set apt ubuntu mirror on `/etc/apt/sources.list` to
  [http://kambing.ui.ac.id/ubuntu](http://kambing.ui.ac.id/ubuntu)
- Set locale settings, LANG to `en_US.UTF-8` and LANGUAGE to `en_US:`
- Set timezone to `Asia/Jakarta`
- Install some utility packages
    - curl
    - debconf
    - dmidecode
    - htop
    - iftop
    - iotop
    - pciutils
    - screen
    - sysstat
    - tmux
    - vim
    - wget

## Requirements

None.

## Role Variables

See `defaults/main.yml` from each dependency role.

## Dependencies

- cecepm.apt
- cecepm.locale
- cecepm.ntp
- cecepm.utils

## Example Playbook

Using default vars

    - hosts: server
      roles:
      - cecepm.ubuntu_common

## License

MIT / BSD

## Author Information

This role was created in 2014 by [Cecep Mahbub](http://ngadimin.org/).
