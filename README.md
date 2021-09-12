# Vagrant + Ansible + Kali

This is a starting point for your own Kali configuration using Vagrant, Ansible, and Kali. Ideally, you would fork this repo and configure Ansible to install your favorite Kali tools and shared folders.

VMware Fusion is the virtual environment in use here but the Vagrantfile can be easily modified for VMware Workstation or VirtualBox.

After you run Vagrant and Ansible, you'll have a Kali VM with a bridged connection. 

## Install Vagrant

```
brew install vagrant
```
## Install Vagrant VMware Utility

https://www.vagrantup.com/vmware/downloads

## Install the Vagrant VMware provider plugin

```
vagrant plugin install vagrant-vmware-desktop
```

## Clone the repo and run vagrant up

```
git clone https://github.com/nojanath/vagrant-ansible-kali
cd vagrant-ansible-kali
vagrant up
vagrant ssh
```

## Kali Credentials

vagrant/vagrant

https://www.kali.org/docs/introduction/default-credentials/







