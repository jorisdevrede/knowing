# Ansible Basic Structure

## Overview
 

## Run
To run this use one of the following options:
```
# Perform a full site deployment in the production environment
$ ansible-playbook -i env_prd/hosts.ini site.yml

# Perform a deployment on a single host in production
$ ansible-playbook -i env_prd/hosts.ini -l server3.prodcution.com site.yml

# Perform a service_b deployment in the test environment
$ ansible-playbook -i env_tst/hosts.ini service_b.yml

# Test a full site deployment on the local host
$ ansible-playbook -i env_lcl/hosts.ini site.yml

```

