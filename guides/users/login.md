# COOL User Login #

## Table of contents ##

* [Pre-requisites](#pre-requisites)
* [First-time Viscosity configuration](#first-time-viscosity-configuration)
* [Connect to the COOL VPN](#connect-to-the-cool-vpn)
* [Connect to the Guacamole remote desktop environment](#connect-to-the-guacamole-remote-desktop-environment)

## Pre-requisites ##

1. You have access to the internet.
1. You have a laptop with Viscosity VPN software installed.
1. You have imported the "CISA COOL" Viscosity connection bundle that was sent
to you via email.
1. You have a PIV (Personal Identity Verification) card.
1. You know the PIN to unlock your PIV.

## First-time viscosity configuration ##

NOTE: These steps only need to be done once, before the first time you connect
to the COOL VPN.

1. Insert your PIV into your PIV reader.
1. Open the Viscosity preferences on your laptop.
1. Select the "CISA COOL" connection and click the "Edit" button.
   <div align="left">
   <img width="460" src="https://raw.githubusercontent.com/cisagov/cool-system/develop/assets/images/viscosity_conn_list.png">
   </div>
1. Click on the "Authentication" tab.
1. In the "PKCS11" section, change the "Retrieval" drop-down menu to
   "Use certificate name below".
1. Click the "Detect" button.
   <div align="left">
   <img width="460" src="https://raw.githubusercontent.com/cisagov/cool-system/develop/assets/images/viscosity_detect_button.png">
   </div>
1. Ensure that the drop-down menu displays your PIV's first certificate, then
   click the "Select" button.
   <div align="left">
   <img width="460" src="https://raw.githubusercontent.com/cisagov/cool-system/develop/assets/images/viscosity_select_cert.png">
   </div>
1. Click the "Save" button.

## Connect to the COOL VPN ##

1. Insert your PIV into your PIV reader.
1. Open the Viscosity preferences on your laptop.
   <div align="left">
   <img width="460" src="https://raw.githubusercontent.com/cisagov/cool-system/develop/assets/images/viscosity_conn_list.png">
   </div>
1. Right-click on "CISA COOL” connection and select “Connect”.
1. When you are prompted with “OpenVPN requires a password to continue.”,
   enter the PIN associated with your PIV and click "OK".  **Do NOT select
   the “Remember details in my Keychain” checkbox.**
   <div align="left">
   <img width="460" src="https://raw.githubusercontent.com/cisagov/cool-system/develop/assets/images/viscosity_pin_prompt.png">
   </div>
1. If everything worked correctly, Viscosity should show that you are
   connected to the COOL VPN.
   <div align="left">
   <img width="460" src="https://raw.githubusercontent.com/cisagov/cool-system/develop/assets/images/viscosity_connected.png">
   </div>

## Connect to the Guacamole remote desktop environment ##

1. After you have connected to the COOL VPN, open the Chrome browser on your
   laptop and go to
   [https://guac.env0.cool.cyber.dhs.gov/](https://guac.env0.cool.cyber.dhs.gov/).
1. If this is your first time visiting that URL, Chrome should prompt you
   about sharing your local clipboard with this site.  Select “Allow” to
   enable seamless copy/paste functionality between your laptop’s host OS
   and the remote instances that you access with Guacamole.
   <div align="left">
   <img width="360" src="https://raw.githubusercontent.com/cisagov/cool-system/develop/assets/images/guac_chrome_allow_clipboard.png">
   </div>
1. Enter the Guacamole username and password provided by the COOL admins,
   then hit the “Login” button.
   <div width="300" align="left">
   <img src="https://raw.githubusercontent.com/cisagov/cool-system/develop/assets/images/guac_login.png">
   </div>
1. To connect to a remote system, locate its name in the list under
   **“ALL CONNECTIONS”** and click on it.  Note that some connections will
   allow you to control the cursor on the remote instance, while other
   connections are “View Only”.
   <div align="left">
   <img width="260" src="https://raw.githubusercontent.com/cisagov/cool-system/develop/assets/images/guac_all_connections.png">
   </div>
1. While connected to a remote system, you should be able to use the
   system as you would any other remote desktop.  Refer to the
   [Guacamole user documentation](https://guacamole.apache.org/doc/gug/using-guacamole.html)
   for full details.  Some useful features of Guacamole are:
   * [Viewing/hiding the Guacamole menu while connected to a remote system.](https://guacamole.apache.org/doc/gug/using-guacamole.html#guacamole-menu)
   * [Copying/pasting text between your local system and the remote system.](https://guacamole.apache.org/doc/gug/using-guacamole.html#using-the-clipboard)
   * [Transferring files between your local system and the remote system](https://guacamole.apache.org/doc/gug/using-guacamole.html#file-transfer)
     (including drag and drop copying from your local system to the remote
     system, but not vice versa).  Files copied to the remote system can be
     found in the `/home/vnc/Documents` directory.
     <div align="left">
     <img width="460" src="https://raw.githubusercontent.com/cisagov/cool-system/develop/assets/images/guac_file_transfer.png">
     </div>
1. To disconnect from the remote system, press **CTRL-OPT-SHIFT**
   (or **CTRL-ALT-SHIFT**) to bring up the Guacamole menu, then select
   the dropdown menu (with your Guacamole username) in the upper-right
   corner and select “Disconnect”.
   <div align="left">
   <img width="460" src="https://raw.githubusercontent.com/cisagov/cool-system/develop/assets/images/guac_disconnect.png">
   </div>
   At that point, you will have the option of returning to the Guacamole
   home screen (if you want to log on to a different remote system) or
   logging out of Guacamole entirely.
   <div align="left">
   <img width="400" src="https://raw.githubusercontent.com/cisagov/cool-system/develop/assets/images/guac_disconnected.png">
   </div>
