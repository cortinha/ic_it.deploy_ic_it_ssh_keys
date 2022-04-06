IC-IT ssh keys deployment
=========

This role intends to install the ssh keys used by the IC-IT team into the authorized_keys file.

Requirements
------------

You should have a github repository hosting the ssh keys.

Role Variables
--------------

|| name || description || default ||
| ----- |  ----------- | --------- |
| user_to_deploy_ssh_keys | for which user do we want to deploy the ssh keys? | root |
| github_user | username of the github account | EPFL-IC |
| github_repo | repository name | ic-it-authorized-keys |

Example Playbook
----------------

```yaml
    - hosts: servers
      roles:
         - { role: ic_it.deploy_ic_it_ssh_keys, user_to_deploy_ssh_keys: vagrant }
```

License
-------

BSD

Author Information
------------------

Emmanuel Jaep [EPFL profile](https://people.epfl.ch/emmanuel.jaep)
