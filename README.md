Ansible Thumbor Centos
====================

*WIP* This is an adaptation of [ansible-thumbor](https://github.com/jivesoftware/ansible-thumbor)
but for CentOS and its wonderfully crappy package manager.

Changes
-------------
- Works with CentOS (and possibly other flavours of Redhat)
- More Thumbor configuration options available through Ansible variables (see `site.yml` and `roles/ansible-thumbor/defaults/main.yml`)

Vagrant
-----------
- Run `vagrant up` from the root directory. Ensure you have the latest Ansible and Vagrant installed.
- It will likely hang at `restart iptables` but everything should be fine.
