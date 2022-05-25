## Setup HTTPD Web server

This playbook shall setup HTTPD web server and samle HTML file at root of the web server.

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
