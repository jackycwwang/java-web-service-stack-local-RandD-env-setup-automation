# Automated Provisioning

This section describes the automated provisioning process.

## Introduction

The automated provisioning is done by adding each of the following lines to each VM defined in the Vagrantfile.

```vagrant
db01.vm.provision "shell", path: "mysql.sh"
mc01.vm.provision "shell", path: "memcached.sh"
rmq01.vm.provision "shell", path: "rabbitmq.sh"
app01.vm.provision "shell", path: "tomcat.sh"
web01.vm.provision "shell", path: "nginx.sh"
```

The `path:` parameter above specifies the path to the provisioning script. Please refer to the following links for more information on each script:

- [MySQL](mysql.sh)
- [Memcached](memcached.sh)
- [RabbitMQ](rabbitmq.sh)
- [Tomcat](tomcat.sh)
- [Nginx](nginx.sh)

## Before Provisioning

Before starting the automated provisioning, It is recommended to destroy all the VMs spinned up previously in the manual provisioning section. Execute the following commands in Git Bash:


```bash
cd vagrant/manual
vagrant destroy --force
vagrant global-status --prune
```

## Provisioning

CD into `vagrant/auto` directory and execute `vagrant up`. A successful execution will bring the command prompt back to the user.


## Validation

Run `http://web01` or `http://192.168.56.11` in the browser and login with the following credentials:
username: `admin_vp`
password: `admin_vp`


The same homepage as the manual provisioning section should be displayed.
