# Hardening Dell BIOS
## Dell Latitude 7490
### BIOS Overview
* General
  * System Information
  * Battery Information
  * Boot Sequence
  * Advanced Boot Options
  * UEFI Boot Path Security
  * Date/Time
* [System Configuration](#system-configuration)
  * Integrated NIC
  * SATA Operation
  * Drives
  * SMART Reporting
  * USB Configuration
  * Dell Type-C Dock Configuration
  * [USB PowerShare](#usb-powershare)
  * Audio
  * Keyboard Illumination
  * Keyboard Backlight Timeout on AC
  * Keyboard Backlight Timeout on Battery
  * Unobtrusive Mode
  * Miscellaneous Drives
* Video
  * LCD Brightness
* [Security](#security)
  * [Admin Password](#admin-password)
  * [System Password](#system-password)
  * Strong Password
  * Password Configuration
  * Password Bypass
  * Password Change
  * Non-Admin Setup Changes
  * UEFI Capsule Firmware Updates
  * TPM 2.0 Security
  * Absolute®
  * OROM Keyboard Access
  * Admin Setup Lockout
  * SMM Security Mittigation
* Secure Boot
  * Secure Boot Enable
  * Secure Boot Mode
  * Expert Key Management
* Intel® Software Guard Extensions™
  * Intel® SGX™ Enable
  * Enclave Memory Size
* Performance
  * Multi Core Support
  * Intel® SpeedStep™
  * C-States Control
  * Intel® TurboBoost™
  * HyperThread control
* Power Management
  * AC Behavior
  * Enable Intel Speed Shift Technology
  * Auto On Time
  * USB Wake Support
  * Wireless Radio Control
  * Wake on LAN/WLAN
  * Block Sleep
  * Peak Shift
  * Advanced Battery Charge Configuration
  * Primary Battery Charge Configuration
  * Type-C Connector Power
* POST Behavior
  * Adapter Warnings
  * USB-C Warnings
  * Keypad (Embedded)
  * Numlock Enable
  * Fn Lock Options
  * Fastboot
  * Extend BIOS POST Time
  * Full Screen Logo
  * Warnings and Errors
  * MAC Address Pass-Through
* Manageability
  * Intel AMT Capability
  * USB Provision
  * MEBx Hotkey
* Virtualization Support
  * Virtualization
  * VT for Direct I/O
  * Trusted Execution
* Wireless
  * Wireless Switch
  * Wireless Device Enable
* Maintenance
  * Service Tag
  * Asset Tag
  * BIOS Downgrade
  * Data Wipe
  * BIOS Recovery
* System Logs
  * BIOS Events
  * Thermal Events
  * Power Events

### General
#### Battery Information
![WIN_20250306_21_48_55_Pro](https://github.com/user-attachments/assets/3323d4ad-1bcd-46b1-95c2-ed9f0bc9c333)

### System Configuration
#### USB Configuration
By default the "Enable USB Boot Support" is checked. For security reasons it is recommended to uncheck this temporarily. If it's needed to boot e.g. a live image or an installer from an USB-Stick, this option must be actived at first for the time of use. After that this option should deactived again.

![WIN_20250309_21_12_27_Pro](https://github.com/user-attachments/assets/ac921989-55c0-449b-ba79-42e6cc79dfb2)

#### USB PowerShare
Even it is only to charge up e.g. your phone over the usb when the system is in sleep mode, deactive useless firmware functions. If you whant to power up a device just use the normal power outlet.

![grafik](https://github.com/user-attachments/assets/6fff036b-18de-4115-a844-4b4817276b1b)


### Security
#### Admin Password
The admin password needs to be enter when the UEFI setup is opened, to do changes on the configurations. By default, no admin password is set. Set a password that matches the company password policies.

![WIN_20250310_21_33_01_Pro](https://github.com/user-attachments/assets/5de30213-18d2-49a3-98f1-ceb20896ab85)

#### System Password
Everytime the system boots, a password must be entered.

![WIN_20250323_22_11_37_Pro](https://github.com/user-attachments/assets/578796ec-d1d0-471e-8223-1e18b86cd58e)
![grafik](https://github.com/user-attachments/assets/f9999196-2b81-400d-b1ea-cbcb7ae8e938)



#### TMP 2.0 Security
![WIN_20250309_20_53_21_Pro](https://github.com/user-attachments/assets/e49c1504-4a6a-45e3-93a4-db6cc83249be)

### Secure Boot
#### Secure Boot Enable
Enables Secure Boot, where the BIOS authenticates each pre-boot image file by using the certificates in the Secure Boot Policy. 
By default, Secure Boot is set to Disabled. Set the Secure Boot feature to Enable.

![WIN_20250309_00_38_59_Pro](https://github.com/user-attachments/assets/b3b3a7f4-c174-411d-887b-68dda0a37bdf)

#### Secure Boot Mode
Configures how the BIOS uses the Secure Boot Policy Objects (PK, KEK, db, or dbx).

Deployed Mode (default): Deployed Mode is the most secure mode. In Deployed Mode, PK must be installed, and the BIOS performs signature verification on programmatic attempts to update policy objects. Deployed Mode restricts the programmatic mode transitions.

Audit Mode: In Audit Mode, PK is not present. BIOS does not authenticate programmatic update to the policy objects and transitions between modes. The BIOS performs a signature verification on pre-boot images and logs the results in the image Execution Information Table but executes the images whether they pass or fail verification. Audit Mode is useful for programmatic determination of a working set of policy objects.

![WIN_20250309_00_45_49_Pro](https://github.com/user-attachments/assets/2e1974dd-43e2-48f3-ad36-b4b69468d164)

#### Expert Key Management
When Secure Boot policy is set to Standard, the BIOS uses the system manufacturer’s key and certificates to authenticate pre-boot images. When Secure Boot policy is set to Custom, BIOS uses the user-defined key and certificates. By default, the Secure Boot policy is set to Standard. So the "Enable Custom Mode" sould be unchecked.

![WIN_20250309_00_57_12_Pro](https://github.com/user-attachments/assets/fc11d20c-8ce9-4062-9d05-d3502e0a67fd)
