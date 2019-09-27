# **Loop Battery Bypass**
## Instructions
Flash the release zip in Magisk through the modules menu and restart the phone. 

You will need xDrip+ and/or AndroidAPS installed as system applications, which can be done through [this Magisk module](https://github.com/Magisk-Modules-Repo/terminal_systemizer). Install that module, restart the phone, access a terminal emulator of some kind and enter the command `systemize`. Follow the on-screen options to systemize the apps you want this module to be able to exclude from battery optimizations, and afterwards restart the phone.

## Description
This module will add two sysconfig files that excludes both xDrip+ and AndroidAPS (as system applications) from any battery optimization, location throttling, and data usage caps that the Android system imposes on the app. 

For whatever reason there seems to be a difference between "Don't optimize" and "Battery optimization not available", as stated [here](https://developer.android.com/training/monitoring-device-state/doze-standby#support_for_other_use_cases). Apps which are in the "Don't optimize" are partially exempt from doze compared to apps which don't have optimization available (like Google Play Services). 

Most of the idea came from [this Stack Overflow post](https://android.stackexchange.com/questions/143247/how-to-make-google-play-services-and-other-default-white-listed-system-apps-doze), which gives useful information on how the doze bypassing works for Google Play Services.

## Requirements
- Android 5.0+
- Magisk
- xDrip+ and / or AndroidAPS installed as system apps