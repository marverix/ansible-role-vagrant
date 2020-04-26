# Ansible Role: Vagrant

[![Build Status](https://travis-ci.com/marverix/ansible-role-vagrant.svg?branch=master)](https://travis-ci.com/marverix/ansible-role-vagrant)
![Ansible Quality Score](https://img.shields.io/ansible/quality/48205)
![Ansible Role](https://img.shields.io/ansible/role/48205)
[![License: ISC](https://img.shields.io/badge/License-ISC-blue.svg)](LICENSE)

Ansible role that installs Vagrant on Linux.

## Features

- ✔️ Installing Vagrant
  - Does the package's checksum check
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
`vagrant_package_checksum` | SHA256 checksums for packages | *checksums for 2.2.7 version*

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
            vagrant_package_checksum:
              deb: 4dec711612c4350733e01745ab9f5acee2fbf9756ab9728b19a4664cae5c275d
              rpm: 1826ff2220951766b65d549f3e6e38f1eb07ff0b4c66197582b1ce62f9104035
    ```

    Note: Here is a list of all released Vagrant versions https://releases.hashicorp.com/vagrant/

## License

ISC
