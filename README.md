# Ansible Ubuntu setup
Ansible roles to setup Ubuntu desktop and Ubuntu server (14.04 and 16.04). This playbook is focused on quickly deploying a "ready to use" dev machine.


## Requirements
- Git
- Ansible 2+ (automatically installed from [Ansible offical PPA](https://launchpad.net/~ansible/+archive/ubuntu/ansible) with the provided install.sh script)


## Installation
First, you need to install Git and Ansible :
```
sudo apt-get install git
git clone https://github.com/Benoth/ansible-ubuntu.git
cd ansible-ubuntu
./install.sh
```

Then you need to customize the playbook `ansible-desktop.yml` (or create a new one) to suit your needs. Every roles are disabled by default.

Run `ansible-playbook ansible-desktop.yml --ask-become-pass` and enter your sudo password to run the playbook

## Roles included

| Role                     | Description                                                                                                                                                                                                                                                                                                                           |
| ------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| | **Desktop tools** |
| firefox                  | Install [Firefox](https://www.mozilla.org/firefox/) (no particular settings, basic installation)                                                                                                                                                                                                                                      |
| skype                    | Install [Skype](https://www.skype.com/)                                                                                                                                                                                                                                                                                               |
| | **Services & server tools** |
| docker                   | Install [Docker](https://www.docker.com/) and Docker compose from Docker deb repository                                                                                                                                                                                                                                               |
| elasticsearch            | Install [Elasticsearch](http://elastic.co/) from Elastic deb repository                                                                                                                                                                                                                                                               |
| nginx                    | Install [nginx](https://nginx.org/) and remove defaults hosts                                                                                                                                                                                                                                                                         |
| nginx-php-fpm            | Basic nginx PHP-FPM Virtualhosts creation (you may need to run the "php" role first, depending on your configuration)                                                                                                                                                                                                                 |
| nodejs                   | Install [NodeJS](https://nodejs.org/en/) from Node deb repository                                                                                                                                                                                                                                                                     |
| python                   | Install [Python](https://www.python.org/)                                                                                                                                                                                                                                                                                             |
| redis                    | Install [Redis](http://redis.io/)                                                                                                                                                                                                                                                                                                     |
| ruby                     | Install [Ruby](https://www.ruby-lang.org/) from [Brightbox PPA](https://launchpad.net/~brightbox/+archive/ubuntu/ruby-ng)                                                                                                                                                                                                             |
| ssh                      | Install [OpenSSH Server](http://www.openssh.com/)                                                                                                                                                                                                                                                                                     |
