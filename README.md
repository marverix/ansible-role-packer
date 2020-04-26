# Ansible Role: Packer

[![Build Status](https://travis-ci.com/marverix/ansible-role-packer.svg?branch=master)](https://travis-ci.com/marverix/ansible-role-packer)
![Ansible Quality Score](https://img.shields.io/ansible/quality/48205)
![Ansible Role](https://img.shields.io/ansible/role/48205)
[![License: ISC](https://img.shields.io/badge/License-ISC-blue.svg)](LICENSE)

Ansible role that installs Packer on Linux.

## Features

- ✔️ Installing Packer
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
`packer_version` | Version of Packer to be installed | `1.5.5`
`packer_package_checksum` | SHA256 checksums for packages | *checksum for 1.5.5 version*

## Dependencies

None

## Example Playbook

1. The simplest one

    ```yml
    ---
    - hosts: all
      roles:
        - marverix.packer
    ```

1. Install Packer 1.1.1

    ```yml
    ---
    - hosts: all
      roles:
        - role: marverix.packer
          vars:
            packer_version: 1.1.1
            packer_package_checksum: e407566e2063ac697e0bbf6f2dd334be448d58bed93f44a186408bf1fc54c552
    ```

    Note: Here is a list of all released Packer versions https://releases.hashicorp.com/packer/

## License

ISC
