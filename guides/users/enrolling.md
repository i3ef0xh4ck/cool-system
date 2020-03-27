# User Enrollment #
<!-- markdownlint-disable MD026 -->

## Who can be a COOL user? ##

We are currently enrolling federal employees and contractors from CISA
Vulnerability Management into the COOL as testers.

## Begin your enrollment. ##

Access to the COOL requires PIV authentication.  In order for us to authorize
your PIV we need you to send us the issuer and subject from your PIV's
public certificate.

*Note:* The following instructions are Mac-specific but they should be easily
adapted to other environments.

Steps:

1. Insert your PIV into the reader attached to your machine.
1. On the same machine, open the
[Terminal](https://support.apple.com/guide/terminal/welcome/mac) and run the
following command to copy your public key to the clipboard:

  ```console
  pkcs15-tool --read-certificate 1 | pbcopy
  ```

1. Create a new email to
[cisa-cool-group@trio.dhs.gov](mailto:cisa-cool-group@trio.dhs.gov?subject=[GitHub]%20COOL%20Access%20Request)
and paste in the certificate data.

Once we have received your information we'll contact you with a few additional
steps to complete your COOL enrollment.
