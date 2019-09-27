# **Loop Battery Bypass**
## Description
This module will add two sysconfig files that excludes both xDrip+ and AndroidAPS from any battery optimization, location throttling, and data usage caps that the Android system imposes on the app. 

For whatever reason there seems to be a difference between "Don't optimize" and "Battery optimization not available", as stated [here](https://developer.android.com/training/monitoring-device-state/doze-standby#support_for_other_use_cases). Apps which are in the "Don't optimize" are partially exempt from doze compared to apps which don't have optimization available (like Google Play Services). 

Most of the idea came from [this Stack Overflow post](https://android.stackexchange.com/questions/143247/how-to-make-google-play-services-and-other-default-white-listed-system-apps-doze), which gives useful information on how the doze bypassing works for Google Play Services.

## Requirements
- Android 5.0+
- Magisk
- xDrip+ and / or AndroidAPS