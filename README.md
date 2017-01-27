Role Name
=========

OU Libraries ngrok Server.

Requirements
------------

If you are using this role, it's because you are hoping to make your local web service accessible from the internet.  That means that you need a local web server (such as apache, nginx, or tomcat) to connect to.

Role Variables
--------------

Expects ngrok_authtoken.  Get one at [ngrok.com](https://ngrok.com/signup)
There is no default for this value, because that wouldn't work.

Things with defaults:

```
ngrok_dir: '/opt/oulib/ngrok'

tunnels:
  - name: 'example'
    dn_suffix: 'ngrok.io'
    port: '443'
    proto: 'tls'
```

This would get you a tls tunnel at:
example.ngrok.io

You can add multiple entries under tunnels. Each entry requires name, dn_suffx, port, and proto as shown.

Dependencies
------------

Requires OU Libraries centos7 role. To install:
```
ansible-galaxy install -r requirements.yml
```

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

Usage
-----

Creates a service called oulib-ngrok, which starts on boot.  All configured tunnels are fired on service start.


License
-------

TBD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
