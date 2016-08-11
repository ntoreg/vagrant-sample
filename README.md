## Sample of Vagrantfile for vagrant-cloudstack

### Prepare

```
$ brew cask vagrant
$ brew cask dotenv
$ vagrant plugin install vagrant-cloudstack
$ vagrant plugin install dotenv
```

### Edit .env

```
CS_HOST = 'compute.jp-east.idcfcloud.com'
CS_API_KEY = 'xxx'
CS_SECRET_KEY = 'xxx'
CS_ZONE = 'newton'
CS_NETWORK = 'newton-network1'
CS_PF_IP_ADDRESS = '1.1.1.1'
CS_PF_PUBLIC_PORT = '2201'
VM_NAME = 'vagrant-sample'
VM_DISPLAY_NAME = 'vagrant-sample'
CS_TEMPLATE = 'CentOS 7.2 64-bit for Vagrant'
CS_SERVICE_OFFERING = 'light.S1'
CS_SSH_KEYPAIR = 'Default'
VAGRANT_SSH_USERNAME = 'vagrant'
VAGRANT_SSH_PRIVATE_KEY = '~/.ssh/id_rsa'
```

### Usage

```
$ vagrant up
$ vagrant ssh
$ vagrant destroy
```

