# Ansible configuration<br>Simple Symfony Application

This ansible config is just a sample, do not use in production!

```
                   ___,                 _    _       ___               _
                  /   |              o | |  | |     / (_)             | | o
  _  _  _        |    |   _  _    ,    | |  | |  _ |      __   _  _   | |     __,
 / |/ |/ |  |   ||    |  / |/ |  / \_| |/ \_|/  |/ |     /  \_/ |/ |  |/  |  /  |
   |  |  |_/ \_/|/\__/\_/  |  |_/ \/ |_/\_/ |__/|__/\___/\__/   |  |_/|__/|_/\_/|/
               /|                                                     |\       /|
               \|                                                     |/       \|
```

![Screen shot - Ansible](https://raw.githubusercontent.com/Remiii/remiii-ansible-ubuntu-app-simple-symfony/master/_documentation/image/image1.png)<br>
Ansible.

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

Setup the vars in `vars/myConfig.yml` and add `ansible_inventory_machinename` file.

For exemple (is just a sample):
```
# ansible_inventory_machinename
machine ansible_ssh_host='127.0.0.1' ansible_ssh_port=10022
```

Copy the config dist file `vars/myConfig.yml.dist`
```sh
$ cp vars/myConfig.yml.dist vars/myConfig.yml
```

```
# pathToTheProject/vars/myConfig.yml
    ...
    rootPath: '~/git/remiii-ansible-ubuntu-app-simple-symfony'
    hostname: 'vm1.local'
    publicIpAddress: '127.0.0.1'
    ...
```

## Add vars

Add the folowing files in the `vars` directory:

- myGitHubUserMachineUserKey - [Some info about GitHub UserMachine](https://developer.github.com/guides/managing-deploy-keys/#machine-users)
- myGitHubUserMachineUserKey.pub - [Some info about GitHub UserMachine](https://developer.github.com/guides/managing-deploy-keys/#machine-users)
- mySSHPublicKey.pub

... TBD

## Run

* Ansible

```sh
$ ansible-playbook -i ansible_inventory_machinename --private-key=~/.ssh/myFuckingPrivateKey.pem -u yourDefaultUser ./myConfig.yml
```

Sample command line for Vagrant:

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

Licensed under the MIT license (see LICENSE.md file)

## Author

* Rémi Barbe (aka Remiii)


