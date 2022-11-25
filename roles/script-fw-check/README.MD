##Role that distributes firewall control script##

----------

The script checks who is the WAN interface (looks at src-nat, dhcp-client, interface name) and checks if there is a drop rule in input and forward.
Sends email alerts.
Must be used in conjunction with a role that configures email on the RouterBoard


In the files/fw-check.rsc file, you need to specify which email to send notifications to.