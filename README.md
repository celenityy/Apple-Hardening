# Apple-Hardening

A collection of hardened Apple configuration profiles to enhance the privacy, security, & overall experience of your device.

## Instructions

1. **Regardless of your device & any instructions below**, install `Hardening-Shared.mobileconfig`.

### iOS

1. Install `Hardening-Shared.mobileconfig`.

2. Depending on your personal preference, install either `iOS-Base.mobileconfig` **or** `iOS-Extended.mobileconfig`. **Do NOT install both.** 

**Extended** is more private & secure, but it may cause breakage & issues depending on your use case. Services such as iCloud, Find My, Siri, Books, Apple TV, & News are completely disabled where possible.

3. Install `DNS.mobileconfig` & select a DNS provider of your choice. **Quad9** is generally recommended for most users, as it is ran by a Switzerland-based non-profit with a very strong privacy policy & track record, and offers real-time protection against malicious domains.

4. You can also optionally install `DNS-Family.mobileconfig` if you wish to restrict access to objectionable content on your device, such as NSFW & gambling.

### macOS

1. Install `Hardening-Shared.mobileconfig`.

2. Install `macOS-Shared.mobileconfig`.

3. Install `macOS-3P.mobileconfig`.

4. Depending on your personal preference, install either `macOS-Base.mobileconfig` **or** `macOS-Extended.mobileconfig`. **Do NOT install both.** 

**Extended** is more private & secure, but it may cause breakage & issues depending on your use case. Services such as iCloud, Find My, Siri, Books, Apple TV, iMessage, FaceTime, & News are completely disabled where possible.

5. Install `DNS.mobileconfig` & select a DNS provider of your choice. **Quad9** is generally recommended for most users, as it is ran by a Switzerland-based non-profit with a very strong privacy policy & track record, and offers real-time protection against malicious domains.

6. You can also optionally install `DNS-Family.mobileconfig` if you wish to restrict access to objectionable content on your device, such as NSFW & gambling.

## Features

### Hardening Shared

* Enforces all domains are subject Certificate Transparency

* Prevents disabling enforcement of Certificate Transparency for any installed certificates

### iOS

#### Base

* Disables Voice Dialing while device is locked

* Enforces encryption of device back-ups

* Blocks apps from requesting to track your activity via ATT (https://support.apple.com/102420 https://developer.apple.com/documentation/apptrackingtransparency)

* Blocks untrusted HTTPS certificates

* Enforces OTA Public-key-infrastructure Updates

* Disables submission of diagnostic data to Apple

* Enables local (on-device) Dictation

* Enables local (on-device) Translation

* Disables Wallet while device is locked

* Disables notification history on lock screen

* Disables Apple's "Personalized Advertising" (https://support.apple.com/105131)

* Requires a device pairing password for outgoing AirPlay requests

* Enforces Fraudulent Website Warning (Safe Browsing) in Safari

* Blocks websites using insecure TLS 1.0 & 1.1 in Safari

* Blocks 3rd party cookies in Safari

* Allows all Movies, TV Shows, & Apps, regardless of age rating

* Allows explicit sexual content in the Books Store

* Blocks Apple Watch from being able to auto-unlock the device

* Prevents Apple from storing audio recordings to improve Siri & Dictation

* Requires setting a PIN or password on the device

* Immediately requires the device passcode once it falls asleep

*For Supervised Devices:*

* Disables Online Siri Suggestions

* Enforces automatic date & time

* Requires authentication via Face or Touch ID for Autofill

* Disables Predictive Keyboard

* Enforces Mail Privacy Protection

* Disables "Personalized Handwriting Results"

* Disallows discovery of AirPrint Printers using iBeacons

* Requires trusted certificates for AirPrint

* Disables Automatic App Downloads (**Not including updates**)

* Disables adding Game Center Friends

* Disables "Remote Screen Observation"

* Blocks Classroom from locking apps or the device without prompting

* Prevents Classroom from automatically joining classes without prompting

* Prevents requiring teacher permission to leave Classroom classes

* Enforces iCloud Private Relay

* Allows playback of explicit music, podcasts, and iTunes U

* Disables Siri's Profanity Filter

* Disables Web Content in Siri

* Blocks defering Software Updates

* Enforces Installation of Rapid Security Responses

* Blocks removing Rapid Security Security Responses

#### Extended

**In addition to everything above in Base:**

* Disables Handoff (Activity Continuation)

* Disables iCloud Backup

* Disables iCloud Keychain Sync

* Disables iCloud Sync for Managed Apps

* Disables iCloud Enterprise Books Backup

* Disables iCloud Enterprise Books, Notes, and Highlights Sync

* Disables iCloud Photo Sharing

* Disables iCloud Photo Library

* Disables iCloud Photo Stream

* Disables Siri

* Prevents use of basic passcodes to unlock device

* Requires alphabetic values in device passcode

*For Supervised Devices:*

* Disables Find My Friends

* Disables Find My Devices

* Prevents pairing with Apple Watch

* Blocks setting up nearby iOS Devices

* Disables Dictation

* Disables iPhone Mirroring

* Disables iPhone Widgets on Mac

* Disables Apple Music

* Disables Apple Bookstore

* Disables Apple News

* Disables Podcasts

* Disables Safari Autofill

* Disables iCloud Document Sync

* Disables requesting passwords from nearby devices

* Disables sharing passwords via AirDrop

### macOS

#### Shared

* Disables Apple's "Personalized Advertising" (https://support.apple.com/105131) & Ad Tracking

* Requires admin permission to install apps from the App Store

* Prevents disabling notifications for software updates

* Disables Bonjour

* Requires authentication for Disc Burning

* Enforces use of FileVault Encryption

* Prevents storing temporary FileVault Keys across restarts

* Sets the system's time server to `time.grapheneos.org`

* Blocks file providers from accessing the path of the requesting process

* Enables hidden files in Finder

* Disables 'Recent Tags' in Finder

* Enables Fast User Switching

* Disables saving documents to iCloud by default

* Enables file extensions in Finder

* Requires setting a password to use the device

* Disables hiding profanity in the system Dictionary

* Disables adding Game Center Friends

* Disables prints including the MAC Address

* Requires admin permission to add printers & print locally

* Requires inputting your password when the device wakes up from sleep

* Requires the password 5 seconds after the device falls asleep

* Automatically re-enables Gatekeeper if disabled (https://support.apple.com/guide/security/gatekeeper-and-runtime-protection-sec5599b66df/web)

* Requires Certificate Trust Validation for Smart Cards & sets to hard-fail

* Disables extended validation checks for TLS certificates

* Automatically checks for updates

* Automatically downloads updates in the background

* Automatically installs macOS updates when available

* Automatically installs App Store updates when available

* Automatically updates XProtect, MRT, & Gatekeeper configuration data

* Automatically installs security updates when available

* Disables macOS Beta releases

* Prevents delaying updates

* Disables submission of diagnostic data to Apple

* Enforces Gatekeeper (https://support.apple.com/guide/security/gatekeeper-and-runtime-protection-sec5599b66df/web)

* Disables Gatekeeper from uploading blocked malware to Apple

* Skips Final Cut Pro Onboarding

* Disables Freeform's iCloud Sign-in Prompt

* Skips GarageBand Onboarding

* Skips Keynote Onboarding

* Disables Home Media Sharing

* Disables Legacy Media Sharing

* Disables Media Sharing

* Skips Numbers Onboarding

* Skips Pages Onboarding

* Enables the 'Develop' Menu in Safari Developer

* Adds extensions to new plain text files in TextEdit

* Sets TextEdit to use plaintext instead of richtext by default

* Skips iMovie Onboarding

* Enforces Automatic Time Synchronization

#### Base

* Disables submission of diagnostic data to Apple

* Enables local (on-device) Dictation

* Disables iTunes File Sharing

* Disables Content Caching

* Disables Apple's "Personalized Advertising" (https://support.apple.com/105131)

* Disables Printer Sharing

* Disables Remote Apple Events Sharing (https://support.apple.com/guide/mac-help/allow-remote-application-scripting-mchlp1398/mac)

* Disables File Sharing

* Disables Internet Sharing

* Disables Remote Management Sharing

* Disables Bluetooth Sharing

* Blocks websites using insecure TLS 1.0 & 1.1 in Safari

* Blocks Apple Watch from being able to auto-unlock the device

* Blocks defering major OS Software Updates

* Requires setting a PIN or password on the device

* Immediately requires the device passcode once it falls asleep

* Prevents Apple from storing audio recordings to improve Siri & Dictation

* Prevents Apple from storing search queries to improve Search

* Enables Built-in Firewall Protection (https://support.apple.com/guide/mac-help/block-connections-to-your-mac-with-a-firewall-mh34041/15.0/mac/15.0)

* Blocks all incoming connections (with exceptions for a couple vital system services & certain apps known to require them)

* Enables Stealth Mode (https://support.apple.com/guide/mac-help/use-stealth-mode-to-keep-your-mac-more-secure-mh17133/mac)

* Disables the 'Tips' App

* Disables the Crash Reporter & Problem Reporter

* Blocks Remote Management Services

* Skips Books Onboarding

* Sets Safari's homepage to the local 'top sites' page rather than `apple.com`.

* Enforces that pages are opened in tabs instead of windows

* Automatically clears Safari's history after one day

* Automatically clears Safari's download history when Safari quits

* Prevents Safari from automatically opening 'safe' downloaded files

* Disables Safari default browser nags

* Disables Bonjour Bookmarks in Safari

* Disables Safari Plug-ins

* Disables Java in Safari

* Blocks JavaScript from automatically opening windows in Safari

* Always asks before submitting insecure forms in Safari

* Blocks 3rd party cookies in Safari

* Enables 'Do Not Track' in Safari

* Blocks websites from sending notifications in Safari

* Enables the 'Develop' Menu in Safari

* Skips iTunes Onboarding (License Agreement)

* Disables sharing iTunes library data with Apple

* Disables "Music Profiles and Posts" in iTunes

* Enforces that iTunes always checks for updates

* Allows explicit Music & Books in iTunes, regardless of age rating

*For Supervised Devices:*

* Disables Online Siri Suggestions

* Disables adding Game Center Friends

* Disables "Remote Screen Observation"

* Blocks Classroom from locking apps or the device without prompting

* Prevents Classroom from automatically joining classes without prompting

* Prevents requiring teacher permission to leave Classroom classes

* Enforces iCloud Private Relay

* Disables Siri's Profanity Filter

* Blocks defering Software Updates

* Blocks defering non-OS Software Updates

* Enforces Installation of Rapid Security Responses

* Blocks removing Rapid Security Security Responses

#### Extended

**In addition to everything above in Base:**

* Disables Handoff (Activity Continuation)

* Disables Universal Control (https://support.apple.com/102459)

* Disables iCloud Keychain Sync

* Disables iCloud Bookmarks

* Disables iCloud Calendar

* Disables iCloud Contacts

* Disables iCloud Desktop & Documents

* Disables iCloud Mail

* Disables iCloud Notes

* Disables iCloud Reminders

* Disables iCloud Photo Library

* Disables iCloud Back to My Mac

* Disables iCloud Freeform

* Disables Siri

* Prevents use of basic passcodes to unlock device

* Requires alphabetic values in device passcode

* Disables AirPlay Receiver

* Disables the 'Siri' App

* Disables the 'Apple TV' App

* Disables the 'Freeform' App

* Disables the 'Home' App

* Disables the 'iPhone Mirroring' App

* Disables the 'Find My' App

* Disables the 'FaceTime' App

* Disables the 'Messages' App

* Disables the 'Podcasts' App

* Disables the 'News' App

* Disables the 'Books' App

* Disables the 'Passwords' App

* Disables the 'Family' App

* Disables the 'iCloud' & 'iCloud+' Apps

* Disables the 'Coverage Details' App

* Disables 'Adobe Core Sync' Apps

* Disables the Books Store

* Disables Contact Bookmarks in Safari

* Disables autofilling web forms, passwords, & credit cards in Safari

* Disables Find My Device

* Disables Device Backups in iTunes

* Disables Apple Music

* Disables Shared Libraries in iTunes

* Prevents iPods, iPhones, & iPads from automatically syncing with iTunes

*For Supervised Devices:*

* Disables FaceTime

* Disables Find My Friends

* Disables Find My Devices

* Disables Dictation

* Disables iPhone Mirroring

* Blocks incoming AirPlay requests

* Disables iMessage

* Disables Apple Music

* Disables Apple Bookstore

* Disables Apple News

* Disables Podcasts

* Disables Safari Autofill

* Disables iCloud Document Sync

* Disables requesting passwords from nearby devices

* Disables sharing passwords via AirDrop