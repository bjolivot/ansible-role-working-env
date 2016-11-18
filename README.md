[![Build Status](https://travis-ci.org/bjolivot/ansible-role-working-env.svg?branch=master)](https://travis-ci.org/bjolivot/ansible-role-working-env)

Working ENV
===========

Init working environnement (user creation, directory )

These directories will be created :

 {{we_working_root_dir}}/
 
    etc
    jar
    log
    opt
    www



Default Values
--------------

we_username: oscaro                     # user name

we_working_root_dir: /oscaro            # working root directory

we_userhome: "/home/{{we_username}}"    # User Home path

we_group: oscaro                        # User Group

we_umask: "0002"                        # User umask


Example Playbook
----------------

Default use: 

    - hosts: server
      roles:
         - working_env

Other use : 

    - hosts: server
      roles:
         - { role: working_env, we_username: "myuser", we_group: "mygroup", we_userhome: "/opt/work" }


License
-------

Licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

