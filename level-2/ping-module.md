**Create Passwordless Authentication**

1. `ssh-keygen -t rsa`
2. `ssh-copy-id steve@stapp02`

**Update inventory file**

```
stapp01 ansible_host=172.16.238.10 ansible_ssh_user=tony
stapp02 ansible_host=172.16.238.11 ansible_ssh_user=steve
stapp03 ansible_host=172.16.238.12 ansible_ssh_user=banner
```

**Test**

`ansible stapp02 -m ping -i /home/thor/ansible/inventory`
