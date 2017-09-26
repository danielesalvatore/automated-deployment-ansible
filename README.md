# automated-deployment-ansible
Automated deployment example, using Ansible and Vagrant

## Run vagrant VM

```
$ cd vagrant
$ vagrant up
``` 

## Ping VM with Ansible
Test if the VM is reachable with Ansible with the command (from the project root):

```
$ ansible webserver -m ping -i ansible/hosts
```


## Deploy web app

```
$ cd ansible
ansible-playbook -i hosts deploy.yml
```

## Generate ssl self signed certificate 

```
$ openssl req -x509 -nodes -days 365 -newkey rsa:1024 -keyout ./ansible/files/ssl/dgms.fao.com.key -out ./ansible/files/ssl/dgms.fao.com.pem

```