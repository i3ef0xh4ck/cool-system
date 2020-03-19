# User Administration #

## Creating a new user with VPN access (CLI) ##

1. Log into a COOL server.
1. Obtain a Kerberos ticket-granting ticket.

  `kinit <username>`

1. Create user:

    `ipa user-add --first Testy --last Testerson --random testy.testerson`

1. Add user to VPN group:

    `ipa group-add-member vpnusers --user testy.testerson`

1. Tail the system log while the user attempts a connection:

    `sudo tail -f /var/log/syslog | grep -A1 "No matching certificate found in LDAP"`

    ```console
    Mar 16 20:57:32 vpn openvpn[690]: VERIFY-CN: WARNING No matching
    certificate found in LDAP Mar 16 20:57:32 vpn openvpn[690]: VERIFY-CN:
    WARNING Searched for: CN=TESTY T TESTERSON,OU=People,OU=DHS HQ,OU=Department
    of Homeland Security,O=U.S. Government,C=US
    ```

1. Add the certificate mapping date for the user using the search string in the log:

    ```console
    ipa user-add-certmapdata testy.testerson "X509:<I>OU=DHS
    CA4,OU=Certification Authorities,OU=Department of Homeland Security,O=U.S.
    Government,C=US<S>CN=TESTY T TESTERSON,OU=People,OU=DHS HQ,OU=Department of
    Homeland Security,O=U.S. Government,C=US"
    ```

1. Destroy the cached Kerberos tickets.

  `kdestroy`

1. Logout
