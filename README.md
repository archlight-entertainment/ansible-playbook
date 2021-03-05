You may be looking for our --> [DOCUMENTATION on wiki](https://github.com/DevelopersPL/otshosting-provisioning/wiki) <--

otshosting-provisioning
=======================
This is an Ansible playbook used to fully provision a Ubuntu machine for OTS Hosting.

__It works with Ubuntu versions with systemd -> Ubuntu >= 20.04__

Make sure to have universe, multiverse and restricted repositories enabled

A script to run on a standalone machine to provision it. If user "arch" does not exist, it will be created with password: "arch".
```bash
#!/bin/bash -ex
apt-get update
apt install -y -q python-simplejson git-core ansible
ansible-pull -i localhost, -U https://github.com/archlight-entertainment/ansible-playbook.git -d /srv/otshosting-provisioning --purge -t default
```
