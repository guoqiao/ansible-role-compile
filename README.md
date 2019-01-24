Ansible Role XBuild
=========

Role name: `guoqiao.xbuild`

A generic Ansible role to build any package from source and install.

While build a package, normally we follow this routine:

- install build dependencies and utils for your system with package manager(apt, yum, dnf, brew, etc)
- git clone repo with specific version(branch, tag, commit)
- configure, compile and install(typically with make)

This role generalize these steps, it could be used to build any version for packages like python, vim, ssh, tmux, nginx, etc.


Installlation
------------

Add it to `requirements.yml`:

    - src: git+https://github.com/guoqiao/ansible-role-xbuild.git
      name: guoqiao.xbuild

Then install from it:

    ansible-galaxy install -r requirements.yml


Refer to [Ansible Galaxy Docs](https://galaxy.ansible.com/docs/using/installing.html).


Requirements
------------

Only support `apt`, `yum` and `dnf` based systems at the moment.

Role Variables
--------------

Refer to [defaults/main.yml](defaults/main.yml)

Dependencies
------------

This role tries to install all dependencies itself.

Example Playbook
----------------

Refer to [tests/test.yml](tests/test.yml)

License
-------

MIT

Author Information
------------------

guoqiao, a Python developer in New Zealand.
