# Welcome to CISA's Cloud Oriented Operations Lab (COOL) #

<div align="center">
<img width="460" src="https://raw.githubusercontent.com/cisagov/cool-system/develop/assets/images/cool_logo.png">
</div>

---

* **You are accessing a U.S. Government information system, which includes
  (1) this computer, (2) this computer network, (3) all computers connected
  to this network and (4) all devices and storage media attached to this
  network or to a computer on this network.  This information system is
  provided for U.S. Government-authorized use only.**
* **Unauthorized or improper use or access of this system may result in
  disciplinary action, as well as civil and criminal penalties.**
* **By using this information system, you understand and consent to the
  following:**
  * **You have no reasonable expectation of privacy when you use this
    information system; this includes any communications or data transiting,
    stored on, originated from or directed to this information system.
    At any time, and for any lawful government purpose, the government may
    monitor, intercept, search and seize any communication or data
    transiting, stored on, originated from or directed to or from this
    information system.**
  * **The government may disclose or use any communications or data
    transiting, stored on, originated from or directed to or from this
    information system for any lawful government purpose.**
  * **You are NOT authorized to process classified information on this
    information system.**

---

## COOL News ##

### April 2nd, 2020 ###

Heads up that we are going to be refreshing the `env0` RPT test environment this
afternoon at **1400 EDT**.  This means that new, updated instances of Guacamole
and Kali will be deployed, along with the underlying services (OpenVPN and
FreeIPA).  Be prepared to lose everything that you had previously set up on the
Kali instances.

The biggest thing that we will be rolling out is a persistent [EFS
volume](https://aws.amazon.com/efs/) that can be accessed by each Kali instance.
This shared storage will be available at `/data` on each Kali.  Note that you
must use `sudo` to create any files or directories within `/data` and assign any
relevant ownership (e.g. make the group owner `vnc` or `kali-trusted` or
whatever).  We can discuss some options to automatically set this up in the
future, but for now, that is how it is.

There are a bunch of other changes being rolled out, but they are mostly under
the covers.  If you have any questions or issues with the **1400 EDT** refresh
today, please let us know ASAP.

### March, 2020 ###

Alpha testing is ongoing- please
  [contact us](https://github.com/cisagov/cool-system/issues/new/choose) if
  you have questions or encounter any issues.

## Quick links for COOL users ##

* [Submit feedback](https://github.com/cisagov/cool-system/issues/new/choose) –
 Found something that needs changing? Open an issue and let us know.

## Contributing ##

We welcome contributions! Please see [here](CONTRIBUTING.md) for
details.

## License ##

This project is in the worldwide [public domain](LICENSE).

This project is in the public domain within the United States, and
copyright and related rights in the work worldwide are waived through
the [CC0 1.0 Universal public domain
dedication](https://creativecommons.org/publicdomain/zero/1.0/).

All contributions to this project will be released under the CC0
dedication. By submitting a pull request, you are agreeing to comply
with this waiver of copyright interest.
