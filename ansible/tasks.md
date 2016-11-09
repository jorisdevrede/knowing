## concatenate hostnames in a group 

```
  - name: use the hosts of an inventory group
    lineinfile:
      dest=/path/file.config
      line="hosts={{ groups.groupname | list | join(', ') }}"
      insertafter=EOF
```
