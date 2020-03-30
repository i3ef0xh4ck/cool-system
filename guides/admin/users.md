# User Administration #

## Creating a new user with VPN access (CLI) ##

1. Log into a COOL server.
1. Obtain a Kerberos ticket-granting ticket.

    `kinit <username>`

1. Create user:

    `ipa user-add --first Testy --last Testerson --random testy.testerson`

1. Add user to VPN group:

    `ipa group-add-member vpnusers --user testy.testerson`

1. Add the certificate mapping data to the user.  You will need the base64
encoded public certificate from the user's `[GitHub] COOL Access Request` email.
This is the data **between** the `-----BEGIN CERTIFICATE-----` and `-----END
CERTIFICATE-----` delimiters.  Exclude the delimiters from the command:

    ```console
    ipa user-add-certmapdata testy.testerson --certificate "MIJH8jCBBtqgBwIB...
    ...
    ...
    /U1di1yoDTI2cJlmmw=="
    ```

1. Destroy the cached Kerberos tickets.

    `kdestroy`

1. Logout
