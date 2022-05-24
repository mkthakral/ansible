## Setup Ansible on Windows

* Download Docker Desktop 
* Pull a Linux container
* Start Container
* Install Ansible
* Create public-private key

```
ssh-keygen -t rsa -C your_email@example.com
```


## Create AWS EC2 instance to be managed by Ansible

* Download "ppk" from Key value pair 
* Open port SSH 22 & HTTP 80
* SSH from Local Windows system to EC2 using "ppk" & EC2 public IP
* Copy public key of Ansible container from /my-user-on-ansible/.ssh/id_rsa.pub
* Paste public key to EC2 /my-user-on-ec2/.ssh/authorized_keys


## Test Connection from Ansible Container to EC2 

```
ssh -i ~/.ssh/id_rsa my-user-on-ec2@ec2-host-or-ip
```

## Setup Ansible Inventory & Playbook
 
  Copy following files to /etc/ansible
  
  * my-hosts
  * my-playbook-web-server-setup.yml
  
 ## Test Playbook
    
  ```
  ansible-playbook my-playbook-web-server-setup.yml -i my-hosts --check
  ```
  
  ## Run Playbook
  
  ```
  ansible-playbook my-playbook-web-server-setup.yml -i my-hosts
  ```
  
  ## Test
  
  * Open in browser: http://ec2-public-ip
  * You should see welcome message 
   
