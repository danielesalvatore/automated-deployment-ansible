# automated-deployment-ansible
Automated deployment example, using Ansible and Vagrant

## Run vagrant VM

```
$ cd vagrant
$ vagrant run
``` 

## Ping VM with Ansible
Test if the VM is reachable with Ansible with the command (from the project root):

```
$ ansible webserver -m ping -i ansible/hosts
```

