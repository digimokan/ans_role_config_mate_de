# ans_role_config_mate_de

Configure the MATE desktop environment.

[![Release](https://img.shields.io/github/release/digimokan/ans_role_config_mate_de.svg?label=release)](https://github.com/digimokan/ans_role_config_mate_de/releases/latest "Latest Release Notes")
[![License](https://img.shields.io/badge/license-MIT-blue.svg?label=license)](LICENSE.md "Project License")

## Table Of Contents

* [Purpose](#purpose)
* [Supported Operating Systems](#supported-operating-systems)
* [Quick Start](#quick-start)
    * [Use From Playbook](#use-from-playbook)
* [Role Options](#role-options)
* [Role Dependencies](#role-dependencies)
* [Contributing](#contributing)

## Purpose

* Install Xorg components.
* Install [MATE Desktop](https://mate-desktop.org/) packages.
* Configure the MATE desktop environment.

## Supported Operating Systems

* Arch Linux.
* FreeBSD.

## Quick Start

### Use From Playbook

1. Create `requirements.yml` in ansible project root, and add this content:

   ```yaml
   # requirements.yml
   - src: https://github.com/digimokan/ans_role_config_mate_de
   ```

2. From the project root directory, install/download the role:

   ```shell
   $ ansible-galaxy install --role-file requirements.yml --roles-path ./roles --force-with-deps
   ```

   * _NOTE:_ `--force-with-deps` _ensures subsequent calls download updates_

3. Include the role like any local role, from the project playbook:

   ```yaml
   # playbook.yml
   - hosts: localhost
     connection: local
     tasks:
       - name: "Configure the MATE desktop environment"
         ansible.builtin.include_role:
           name: ans_role_config_mate_de
         vars:
           user_name: "user2"
   ```

## Role Options

See the role `defaults` file, for overridable vars:

  * [defaults/main.yml](../defaults/main.yml)

Define these _required_ vars for the role:

  * `user_name`: name of primary MATE user to configure the desktop for

## Role Dependencies

* [ans_role_config_sudo](https://github.com/digimokan/ans_role_config_sudo)
* [ans_role_config_xorg](https://github.com/digimokan/ans_role_config_xorg)

## Contributing

* Feel free to report a bug or propose a feature by opening a new
  [Issue](https://github.com/digimokan/ans_role_config_mate_de/issues).
* Follow the project's [Contributing](CONTRIBUTING.md) guidelines.
* Respect the project's [Code Of Conduct](CODE_OF_CONDUCT.md).

