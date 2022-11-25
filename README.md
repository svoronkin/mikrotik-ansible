# mikrotik-ansible
Ansible roles for setup mikrotik devices

----------
Some templates for manage mikrotik devices. For first customize it for you, because there is some temporary logins, passwords, etc.


**Recomendations**
----------
- Create an unprivileged user on the system, for example, mikroansible ` adduser mikroansible`
- Become this user `su - mikroansible`
- Generate `ssh-keygen` RSA key pair
- Install pwgen `apt-get install pwgen` (required by some roles)
- Configure SSH client settings file ~/.ssh/config

----------    
    Host * 
    ServerAliveInterval 4
    ServerAliveCountMax 5
    ConnectTimeout 10
    NumberOfPasswordPrompts 0
    StrictHostKeyChecking yes

----------
- Add routers under Anbsibe control - create an ansible account on the routers and set the public key. Several roles have been prepared for this.

roles/add-to-ansible - Simply creates a user on the router. You need to edit the variables of this role and specify which user and with which key to create.

roles/init - Update and create a user. If the ROS version is < 6.31, it will update to the latest version (via /system packages), update the firmware and add users.

----------
**In order to avoid incomprehensible situations with connecting to equipment, I recommend that you familiarize yourself with the ssh client options in detail**

`NumberOfPasswordPrompts` and `StrictHostKeyChecking`

----------
What this or that role does is clear from the name.

Some roles have their own README. Some has it in Russian language :)

