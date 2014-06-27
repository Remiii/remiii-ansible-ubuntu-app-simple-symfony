# remiii-ansible-ubuntu-app-simple-symfony

This ansible config is just a sample, do not use in production!

## Introduction

Ubuntu server 14.04.

Users system:
- ubuntu or vargrant... (sudo) default user
- $user (sudo)

Users mySQL:
- root
- $user
- websitesample

Mark: sample user `django`.

## Installation

Install Ansible with your package manager (apt, brew...).

## Setup

Setup the vars in myConfig.yml and add `ansible_inventory_machinename` file

```
# ansible_inventory_machinename

machine ansible_ssh_host='127.127.127.127' ansible_ssh_port=22
```

## Run

* Ansible

```sh
$ ansible-playbook -i ansible_inventory_machinename --private-key=~/.ssh/myFuckingPrivateKey.pem -u yourDefaultUser ./myConfig.yml
```

Sample command line for vagrant:

```
$ ansible-playbook -i ansible_inventory_machinename --private-key=~/.vagrant.d/insecure_private_key -u vagrant ./myConfig.yml
```

Sample command line for AmazonEC2:

```
$ ansible-playbook -i ansible_inventory_machinename --private-key=~/.ssh/my-private-key.pem -u ubuntu ./myConfig.yml
```

[Ansible doc](http://docs.ansible.com/guide_vagrant.html#running-ansible-manually)

That's it!

## Setup and run on Vagrant local machine

[In this Gist you can find all the informations in order to setup a Vagrant VM with this Ansible config](https://gist.github.com/Remiii/3857fdca713aebf9f84d).

## License

MIT

## Author

* Rémi Barbe (aka Remiii)


