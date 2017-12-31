
### Environment variables
You can predefine them for your shell in the following ways.
1. `/etc/environment`<br/>
Use this to set for all users. Is specifically for environment variables.

2. `/etc/profile.d/myscript.sh`<br/>
Use this to set for all users. Can combine environment variables with other scripting.

3. `~/.bash_profile` or `~/.bashrc`<br/>
Use this for a single user. Can combine environment variables with other scripting.


#### Create
Bash:`export var='value'`<br/>
Powershell: `$env:var = "value"`

#### Delete
Bash:`unset var`<br/>
Powershell: `Remove-Item env:\var`

#### List
Bash:`env`<br/>
Powershell: `dir env:`


---

### Sudo without password
```bash
$ echo 'ALL            ALL = (ALL) NOPASSWD: ALL' >> /etc/sudoers
```
Or use `sudoedit /etc/sudoers`

---

### Symlink 
```bash
$ ln -sf /path/to/file /path/to/symlink
```