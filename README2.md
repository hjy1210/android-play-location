# LocationUpdatesForegroundService
## Features
1. Service
1. ForegroundService
1. BroadCast and BroadCastReceiver
1. Message with StartActivity and RemoveService features
1. SharedPreference

## Concept
1. Notification object is the second argument of startForegroundService()
1. It seems Activity can't receive broadcast when it is in background.
## Modification
1. Message without StartActivity and RemoveService features
1. In ForegroundService, use less notify

## Note
```
    compileSdkVersion 28
    buildToolsVersion "28.0.2"
       targetSdkVersion 26
```
Above configuration work on Android 8 and 9.
```
    compileSdkVersion 28
    buildToolsVersion "28.0.2"
       targetSdkVersion 28
```
Above configuration work on Android 8 but not Android 9.

## TODO
1. In ForegroundService, change sendBroadcast to save location data in SharedPreference,
1. In Activity.onResume, retrieve above data and clear from SharedPreference.