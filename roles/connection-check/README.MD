# Role to check if Ansible can connect to the router #

----------
Needed to catch errors when connecting RouterOS, such as:

- Change the thumbprint of the ssh server certificate

----------

    @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
    WARNING: REMOTE HOST IDENTIFICATION HAS CHANGED!
    @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
    IT IS POSSIBLE THAT SOMEONE IS DOING SOMETHING NASTY!
    Someone could be eavesdropping o
    n you right now (man-in-the-middle attack)!
    It is also possible that a host key has just been changed.
    The fingerprint for the DSA key sent by the remote host is
    ...

----------
- Wrong username/password
- Missing host in .ssh/known_hosts


----------
Problem alerts by email.

You need to edit tasks\main.yml and provide the correct credentials to connect to the mail server.