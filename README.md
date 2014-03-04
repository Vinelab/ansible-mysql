# Ansible MySQL
Install and configure MySQL on Centos/Red Hat with Ansible

## Installation
Clone this repository inside your ```roles``` directory

## Synopsis
- ```host``` represent ```user@[host]``` from where they are granted access
- ```bind``` is for binding IP addresses allowing remote access to MySQL

## Usage
There must be an ```app``` var with ```mysql``` inside it defined as follows:

```yaml

vars:

  app:
    mysql:
      db: project-database
      user: my-user
      password: najem
      privileges: "*.*:ALL"
      host: %
      bind:
      - 0.0.0.0

```

> you may also specify ```app:``` in a separate YAML file and include it in ```vars_files```