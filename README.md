# Getting Start with Vagrant

This task allowed me to familiarize myself with vagrant and how to set it up.

## How I setup

> Done on my host machine running Ubuntu 22.04

```sh
# On host machine
sudo apt update # update the source files
sudo apt install virtualbox vagrant -y # install virtualbox and vagrant

# vagrant setup
vagrant box add ubuntu/focal64 # downloaded Ubuntu 20.04 image
vagrant init ubuntu/focal64 # create the appropriate Vagranfile

# spin up VM
vagrant up --provider virtualbox

# connect to VM
vagrant ssh
```

## Few observations (Per my setup)

- I needed to use virtualbox version 6.1
  - My later version which was 7.0 wasn't supported so I had to downgrade
- The default username is `vagrant` (obviously).
- The hostname is set to `vagrant-box` by default.
- I used the command `vagrant up --provider virtualbox` to ensure it was really using virtualbox
  - Previously, it was using `libvirt`
- Access to VM was SSH-based

# Customizations

For this particular, it's up to the user to make the changes that suits their
purpose. Feel free to checkout the [official documentation](https://developer.hashicorp.com/vagrant/docs)
