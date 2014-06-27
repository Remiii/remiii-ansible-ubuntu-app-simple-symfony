# remiii-ansible-ubuntu-app-simple-symfony

This ansible config is just a sample, do not use in production!

## Introduction

Ubuntu server 14.04.

Users system:
- ubuntu (sudo) default user
- $user (sudo)

Users mySQL:
- root
- $user
- websitesample

Mark: sample user `django`.

## Installation

Install Ansible.

## Setup

Setup the vars.

## Run

* Ansible

```sh
$ ansible-playbook -i ansible_inventory_machinename --private-key=~/.ssh/myFuckingPrivateKey.pem -u ubuntu ~/git/remiii-ansible-ubuntu-app-simple-symfony/myConfig.yml
```

http://docs.ansible.com/guide_vagrant.html#running-ansible-manually

That's it!

## License

MIT

## Author

* Rémi Barbe (aka Remiii)


