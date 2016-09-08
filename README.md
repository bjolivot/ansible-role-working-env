Working ENV
===========

Init working environnement (user creation, directory )
These directories will be created :
 {{we_userhome}}/
   etc
   jar
   log
   opt
   www


Role Variables
--------------

we_username: User Name  (required)
we_working_root_dir: root directory for working files (required)

we_userhome: User Home directory (optional)
we_usergroups: User group list



Default Values
--------------
we_usergroups:false  
we_userhome:false


Example Playbook
----------------

    - hosts: server
      roles:
         - { role: working_env, we_username: "myuser", we_usergroups: "[group1, group2]", we_userhome: "/opt/work" }


License
-------

Licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

