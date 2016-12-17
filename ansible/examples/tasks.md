## concatenate hostnames in a group 

```
  - name: use the hosts of an inventory group as comma separated list with a host:port syntax
    lineinfile:
      dest: /tmp/testfile
      regexp: "^{{ groups['tokio'][0] }}"
      line: "{{ groups['tokio'] | join(':22, ') }}:22"
      state: present
      insertafter: EOF
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
