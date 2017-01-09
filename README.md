Logrotate
=========

This role install logrotate and manages the main configuration along with the indvidual servieces.

Requirements
------------
None.

Role Variables
--------------

How often to rotate logs (monthly, weekly, daily):

    logrotate_default_rotation: weekly

How far back to keep logs:

    logrotate_default_backlogs: 4

What to do after rotate a log file:

    logrotate_default_after_rotate_action: create

What suffix to use for rotated logs:

    logrotate_default_suffix: dateext

Whether to compress the rotated files:

    logrotate_default_compress: compress

Location of the service files:

    logrotate_default_includes_dir: /etc/logrotate.d

What services to setup for rotation

    logrotate_services: []

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - ansible-role-logrotate

License
-------

MIT
