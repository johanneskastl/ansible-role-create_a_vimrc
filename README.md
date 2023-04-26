![Ansible Lint](https://github.com/johanneskastl/ansible-role-create_a_vimrc/workflows/Ansible%20Lint/badge.svg)

create_a_vimrc
=========

Create a sensible .vimrc

Requirements
------------

None.

Role Variables
--------------

- `additional_users`: (optional) Other users except the root user, that should
  get a ~/.bashrc. A good idea would be to create one for the `ansible_user`...
- ``: (optional) Boolean that decides whether or not `/root/.vimrc` should be
  created (default is `true`)

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
        - role: 'johanneskastl.create_a_vimrc'
          additional_users:
            - "{{ ansible_user }}"
            - 'alice'
            - 'bob'

License
-------

BSD-3-Clause

Author Information
------------------

I am Johannes Kastl, reachable via kastl@b1-systems.de.
