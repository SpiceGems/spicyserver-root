Role Name
=========

Spin servers with a user added along with networking and file related optimization.

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------
# New user to create
USERNAME: ""
# Password of the user
PASS: ""
# Port to use for SSH
SSH_PORT: 22
# Location of swapfile
swap_path: "/swapfile"
# Hosts with low RAM may need to use a small bs size
dd_bs_size_mb: 256
# Total size for swapfile
# Count of how many passes dd should make at bs size
swap_count: 16
# How often swap is utilized 0 to 100
swappiness: 10
# How often inode info is removed from cache
vfs_cache_pressure: 50

Dependencies
------------

Nothing

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: spicegems.spicyserver-root }

License
-------

MIT

Author Information
------------------

Varun Batra <codevarun@gmail.com>