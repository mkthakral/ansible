## Create Linux User

This playbook shall help create a Linux user on remote machines using ansible

## Copy Playbook

Copy that playbook YAML to ansible control machine at

```
/etc/ansible
```

## Run Playbook


```
cd /etc/ansible/
ansible-playbook playbook_create_user.yml -i my-hosts

```

## Test

On remote machines, test

```
sudo su - tomcat
```

You should be able to switch to new user.
