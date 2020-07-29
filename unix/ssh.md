# SSH related stuff

## Create a new key
`ssh-keygen -t rsa -C "your_email@example.com"`

## Stuff that proved helpful on my mac

Create a file ~/.ssh/config And add the following content:
```
Host *
   AddKeysToAgent yes
   UseKeychain yes
   User <remote user>
```

Put your private key in the file ~/.ssh/id_rsa

Permissions for ~/.ssh and ~/.ssh/id_rsa: 700

## Command to run on the remote server
`cd ~ && mkdir .ssh && echo "<content of id_rsa.pub" >> ~/.ssh/authorized_keys