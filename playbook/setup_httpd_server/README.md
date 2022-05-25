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
ansible-playbook playbook-setup-httpd-server.yml -i my-hosts

```

## Test

 * Open in browser: http://ec2-public-ip
 * You should see welcome message 
