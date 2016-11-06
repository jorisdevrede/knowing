# SSH

## How to configure login using SSH keys.

1. log into the client as the user that will perform the remote access

2. generate SSH keys
create a `id_rsa` private and `id_rsa.pub` public key.
```
$ ssh-keygen -q -t rsa -f ~/.ssh/id_rsa -C " -N "
```

3. copy id_rsa.pub to remote system

4. add the public key to authorized keys
```
$ cat id_rsa.pub >> ~/.ssh/authorized_keys
```

5. optionally change the permission on authorized_keys
```
$ chmod 0600 ~/.ssh/authorized_keys
```
