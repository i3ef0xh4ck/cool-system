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

Insert your PIV into the reader attached to your machine.  On the same machine,
open the [Terminal](https://support.apple.com/guide/terminal/welcome/mac) and
run the following command:

```console
pkcs15-tool --read-certificate 1 | \
openssl x509 -noout -subject -issuer -nameopt rfc2253 | pbcopy
```

The command copied the subject and issuer to your clipboard.  Now paste the
result into an email and send it to
[cisa-cool-group@trio.dhs.gov](mailto:cisa-cool-group@trio.dhs.gov?subject=[GitHub]%20COOL%20Access%20Request).

Once we have received your information we'll contact you with a couple
additional instructions to complete your COOL enrollment.
