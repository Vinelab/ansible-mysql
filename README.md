# Ansible MySQL
Install and configure MySQL on Centos/Red Hat/Fedora with Ansible

## Installation

- Clone this repository inside your ```roles``` directory
or add as submodule: `git submodule add git@github.com:Vinelab/ansible-mysql roles/mysql`

- In your playbook:

```yaml
roles:
    - mysql
```


## Synopsis
- ```host``` represents ```user@[host]```
- ```bind``` is for binding IP addresses allowing remote access to MySQL

## Usage

```yaml

vars:

  mysql:
    db: project-database
    user: myuser
    password: passwourld
    privileges: '*.*:ALL'
    host: '%'
    bind:
      - 0.0.0.0

```

> you may also specify ```app:``` in a separate YAML file and include it in ```vars_files```
