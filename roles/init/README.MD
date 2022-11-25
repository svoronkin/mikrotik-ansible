# Role to update the router and add an Ansible user. #

----------

Update and create user. If the ROS version is < 6.31, it will update to the latest version (via /system packages), update the firmware, and add users.


** Be sure to change the password and public key in the file
files/init-script.rsc **

If required, then change the login.