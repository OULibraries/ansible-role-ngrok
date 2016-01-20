Role Name
=========

OU Libraries ngrok Server.

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

Expects ngrok_authtoken.  Get one at [ngrok.com](https://ngrok.com/signup)
There is no default for this value, because that wouldn't work.

We use TLS tunnels, so you'll need a paid account that supports that mode.  If you want to run insecure tunnels, go fish.

Epects ngrok_dn_suffix, which defaults to 'ngrok.io'

Expects sites, which defaults to ['example']
As you can probably guess, you may specify multiple sites.

This would get you a tunnel at:
example.ngrok.io

Dependencies
------------

Requires OU Libraries centos7 and apache2 roles. To install:
```
ansible-galaxy install -r requirements.yml
```

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

TBD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
