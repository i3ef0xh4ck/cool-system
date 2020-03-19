# Setting up LDAP (CLI) #

1. Log into a COOL server.
1. Obtain a Kerberos ticket-granting ticket.

    `kinit <username>`

1. Create VPN users group:

    `ipa group-add --desc="Users that are allowed to connect to the OpenVPN
    servers." vpnusers`

1. Destroy the cached Kerberos tickets.

    `kdestroy`

1. Logout
