# Ansible Role: Vagrant

[![Build Status](https://travis-ci.com/marverix/ansible-role-vagrant.svg?branch=master)](https://travis-ci.com/marverix/ansible-role-vagrant)
![Ansible Quality Score](https://img.shields.io/ansible/quality/47511)
![Ansible Role](https://img.shields.io/ansible/role/47511)
[![License: ISC](https://img.shields.io/badge/License-ISC-blue.svg)](LICENSE)

Ansible role that installs Vagrant on Linux.

## Features

- ✔️ Installing Vagrant
  - You can define which version should be installed
  - Skips if requested version is already installed
- ✔️ Tested with Molecule Verify

## Supported Platforms

- ✔️ Ubuntu 16.04 (Xenial)
- ✔️ Ubuntu 18.04 (Bionic)
- ✔️ CentOS 7

## Requirements

None

## Role Variables

Variable | Description | Default Value
--- | --- | ---
`vagrant_version` | Version of Vagrant to be installed | `2.2.7`

## Dependencies

None

## Example Playbook

1. The simplest one

    ```yml
    ---
    - hosts: all
      roles:
        - marverix.vagrant

    ```

1. Install Vagrant 2.2.2

    ```yml
    ---
    - hosts: all
      roles:
        - role: marverix.vagrant
          vars:
            vagrant_version: 2.2.2
    ```

    Note: Here is a list of all released Vagrant versions https://releases.hashicorp.com/vagrant/

## License

ISC
