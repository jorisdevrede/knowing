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
