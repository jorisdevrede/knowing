## concatenate hostnames in a group 

```
  - name: use the hosts of an inventory group as comma separated list
    lineinfile:
      dest=/path/file.config
      line="hosts={{ groups.groupname | list | join(', ') }}"
      insertafter=EOF
```

## install multiple packages
```
  - name: install multiple packages
    package: name={{ item }} state=latest
    with_items:
      - package1
      - package2
```

## package management
```
  pre_tasks:

# run apt-get update once for an apt based OS.

  - name: update package cache - apt
    apt: update_cache=yes
    when: ansible_pkg_mgr in 'apt'

  tasks:

# run the generic package module for all package management

  - name: manage unzip package
    package: name=unzip state=latest
```
