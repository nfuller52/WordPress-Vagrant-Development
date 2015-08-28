#WordPress & Vagrant Development Environment

This provisioning will create however many virtual machines you want, but the
provisioning has to be run with Ansible on a local machine or another virutal
machine.

##Prerequisits
This project does rely on the hostupdater plugin for vagrant. Easy enough, just
run the following command.

```
$ vagrant plugin install vagrant-hostsupdater
```

##Setting Up Configurations
There isn't too much configuration here, but that's on purpose!

Depending on the amount of machines you want to run you can simply add them
to the hash in the Vagrantfile. Use the format

```
{
  hostname => ip
}
```

## Setup Instructions
Initial installation will take some time as it may need to install the
virtual box.

The initial install will ask for your password, all it's doing is syncing
up the working directory ```app``` with a local directory on the vagrant
machine called ```/vagrant```

Move into the parent directory and run:
```
$ vagrant up
```
You may see the following line in red, don't be alarmed this is just an Ubuntu
tty issue. Everything is working fine!

```
==> hostname: stdin: is not a tty
```