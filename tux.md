
### Environment variables
You can predefine them for your shell in the following ways.
1. `/etc/environment`<br/>
Use this to set for all users. Is specifically for environment variables.

2. `/etc/profile.d/myscript.sh`<br/>
Use this to set for all users. Can combine environment variables with other scripting.

3. `~/.bash_profile` or `~/.bashrc`<br/>
Use this for a single user. Can combine environment variables with other scripting.

```bash
#Create
$ export var='value'

#Delete
$ unset var

#List
$ env
```
---
### Linux release
```bash
$ lsb_release -a
or
$ cat /etc/lsb-release
```

---

### Sudo without password
```bash
$ echo 'ALL            ALL = (ALL) NOPASSWD: ALL' >> /etc/sudoers
```
Or use `sudoedit /etc/sudoers`

---

### Symlink 
```bash
$ ln -sfn /path/to/file /path/to/symlink

$ readlink -f /path/to/symlink
/path/to/file
```

---

### More info
- [The Bash Guide](http://guide.bash.academy)
- [Upstart vs Systemd commands](https://unix.stackexchange.com/questions/5877/what-are-the-pros-cons-of-upstart-and-systemd)
