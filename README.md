jenkins
=======

This role installs and configures [Jenkins](https://jenkins.io/).

Requirements
------------

Only Ubuntu 16.04 (xenial) is supported (no OpenJDK 8 for older LTS)

Role Variables
--------------

- `jenkins_user`: User that will run jenkins (default: 'jenkins')
- `jenkins_group`: Group that will run jenkins (default: jenkins_user)
- `jenkins_home`: Jenkins' home dir (default: '/var/lib/jenkins')
- `jenkins_http_port`: Port Jenkins will listen on (default: '8080')
- `jenkins_state`: Desired daemon state after role execution (default: 'started')

Dependencies
------------

- dpujadas/ansible-role-java

Example Playbook
----------------

    - hosts: servers
      roles:
        - {
          role: jenkins
        }

License
-------

MIT

[![Build Status](https://travis-ci.org/dpujadas/ansible-role-jenkins.svg?branch=master)](https://travis-ci.org/dpujadas/ansible-role-jenkins)
