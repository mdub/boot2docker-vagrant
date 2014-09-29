# localdocker

This is a Vagrant-based boot2docker VM, for local development.

It uses a custom boot2docker image with VirtualBox extensions installed,
allowing sharing of directories (and therefore Docker volumes) with the
underlying host.

## Prerequisites

Vagrant. VirtualBox.

## Usage

Type `vagrant up` to bring the VM up.

The VM gets IP address 192.168.66.3.  Any mapped ports should be visible on that address (rather than localhost).  You might also wish to set up an entry in `/etc/hosts`:

    192.168.66.3 boot2docker

To communicate with the Docker daemon from your host machine, set:

    $ export DOCKER_HOST=tcp://192.168.66.3:4243

Your home directory will be shared with the VM, so mapping volumes should mostly work, as long as they're within $HOME.
