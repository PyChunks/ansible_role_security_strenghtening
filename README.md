Role Name
=========

Makes basic security strenghtening changes mainly related to ssh.

Requirements
------------

This role is dependant on the `Ansible Posix collection` available from Ansible-galaxy.

```
ansible-galaxy collection install ansible.posix
```

Role Variables
--------------
Variables that need to be set:
```
ssh_user:
ssh_user_pass:
```

The variable `ssh_user` needs to be set to the user who is going to have access to the remote server and `ssh_user_pass` is it's associated password.
NB: the password is not used to connect via ssh.

Variables with a default value:

```jinja2
pubkey_path: ~/.ssh/id_rsa.pub
```

Location of the ssh publickey you wish to use to connect to the remote server.
Dependencies
------------

None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - ansible_role_security_strenghtening

License
-------

BSD

Author Information
------------------

Created by Vincent D-Gauthier
