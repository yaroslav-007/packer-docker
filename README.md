# Packer building docker image
Packer that builds docker image box that has nginx

## pre-requirements

- Install **Packer**
	- Download Vagrant from https://www.packer.io/downloads.html
	- Extract the binary file and move/copy it to /usr/local/bin/
	- Check if installed 
		``` packer -v ```
- Install **Docker**
    - Install docker as per ariticle: https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-18-04
- Install **VirtualBox**
    - Execute in terminal: ```sudo apt-get install virtualbox```


## How to run the code
In the terminal run the following commands:

- Build VM with Virtualbox with docker installed
```
    git clone https://github.com/yaroslav-007/packer-docker.git
    cd packer-docker/
    vagrant up
    
```
- Log in the VM and build the docker image
```
    vagrant ssh
    cd /vagrant
    sudo packer build template.json
```