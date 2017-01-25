# 2.2.0 (2017/01/25)

Support [Rich push notification](http://docs.repro.io/en/dashboard/campaign/push-notification.html#media) for Android 4.1~.

# 2.1.22 (2017/01/06)

## Improved

- Add length validation for the User ID and the application version name

## Fixed

- Fixed the possibility of the Exception while tracking the orientation of the device

# 2.1.11 (2016/11/25)

## Fixed

- Fixed the bug where it raises SSL handshake error while connecting to Repro's server

# 2.1.8 (2016/11/17)

## Improved

- Show the dialog type In-App Message larger for devices that has large display

# 2.1.7 (2016/11/09)

## New

- Enable to stop recording during scrolls

## Improved

- Draw masks larger during scrolls

## Fixed

- Fixed the bug where the masking comes sporadically off for an instant right after the web page is loaded

# 2.1.2 (2016/10/13)

## Fixed

- Fixed the size of In-App Message dialog type image

# 2.1.0 (2016/10/05)

## New

- Enable to open Deep Link or Web URL by opening Push Notification

# 2.0.4 (2016/09/01)

## Fixed

- Fixed the bug where it rarely failed to close In-App Message

# 2.0.0 (2016/08/16)

**The special step is required to upgrade the SDK. Please read our [Upgrade Guide](http://docs.repro.io/en/dev/sdk/upgrade/android.html#upgrading-to-android-2-0-0).**

## New

- Add following APIs
  - `setIntUserProfile(String, int)`
  - `setDoubleUserProfile(String, double)`
  - `setDateUserProfile(String, Date)`

## Changes

- `setUserProfile(String, String)` and `setUserProfile(HashMap<String, String>)` was removed. Use `setStringUserProfile(String, String)` instead

# 1.2.9 (2016/07/20)

## Improved

- Prevent uploading the empty movie file
- Remove deprecated API call for recording
- Record In-App message view

# 1.2.0 (2016/06/30)

**The special step is required to upgrade the SDK. Please read our [Upgrade Guide](http://docs.repro.io/en/dev/sdk/upgrade/android.html#upgrading-to-1-2-0).**

## Changes

- Deprecate `setup(String)` API. Use `setup(Application, String)` instead.

## Improved

- Clear the masks for WebView when it transit to the other page

## Fixed

- Fixed the crash when starting the application in some devices
- Fixed the bug where it rarely failed to start recording

# 1.1.47 (2016/06/14)

**If you are using WebView tracking and/or masking, the special step is required to upgrade the SDK. Please read our [Upgrade Guide](http://docs.repro.io/en/dev/sdk/upgrade/android.html#upgrading-to-1-1-47).**

## Improved

- Show the progress dialog while loading the image of the In-App message
- Track WebView event called from immediate function of JavaScript

## Fixed

- Fixed the some layout issue of the In-App message
- Fixed the possibility of the InternalError while starting the Timer
- Fixed the possibility of the ClassCastException while tracking the rotation of the device

# 1.1.37 (2016/06/01)

## Changes

- Deprecate `enableCrashReporting()` API

## Improved

- Improved stability of recording
- Show progress dialog while loading In-App message

# 1.1.29 (2016/05/19)

## Fixed

- Fixed the possibility of NullPointerException while tracking WebView

# 1.1.28 (2016/05/18)

## Fixed

- Fixed the bug where Push Notification was not tracked properly

# 1.1.26 (2016/05/16)

## New

- Add `getDeviceID` and `getUserID` API

## Improved

- Don't overwrite existing notification when receives new GCM message
- Prevent to track touches while pause recording
- Remove dependency to Support.V4
- Limit the length of user profile key and value
- Track In-App Message ID even if the app was killed after showing the Message
- Track CTA event if CTA URL is not specified

# 1.1.14 (2016/04/25)

## Improved

- Improved stability of recording
- Improved stability of displaying In-App message
- Retry configuration if it is failed
- Use default SSLContext to download image

# 1.1.5 (2016/03/31)

## Fixed

- Fixed the bug where Activity.onWindowFocusChanged was interfered by the SDK

# 1.1.4 (2016/03/31)

## Fixed

- Fixed a crash when recording stopped
- Reduced a possibility to upload invalid session data

# 1.1.2 (2016/03/23)

## New

- Enabled to track push notification as opened

## Improved

- Improved thread safety
- Improved stability of uploading

## Fixed

- Fixed delay of session data uploads
- Reduced the possibility to deliver in-app messages already shown
- Fixed the possibility of NullPointerException

# 1.0.1 (2016/03/11)

## Features

- Enable to show in-app message when tracking event

## Improvements

- Improve stability of session and recording

## Bug fixes

- Fix file upload over 4G
- Fix a rare crash after stopping recording while paused
- Fix the format of crash report on Android 4.3 or earlier

# 0.15.0 (2016/03/03)

## Features

- Add Masking API for WebView

## Improvements

- Make a user ID persistent

## Bug Fixes

- Reduce the possibility to upload duplicate session data

# 0.14.5 (2016/02/21)

## Features

- Add crash reporting
- New In-App Message
  - Enables to choose Dialog type
  - Enables to use two buttons in message

## Changes

- Deprecate `track(String JSONObject)` API
  - Use `track(String, Map<String, Object>)` instead

## Bug Fixes

- Fix crashes when the application goes foreground
- Fix crashes while preparing GL
- Fix the bug where the old session data wan't removed correctly

# 0.13.22 (2016/02/11)

## Changes

- Stop trying to upload files when internet connection is not available
- Limit event name length and event properties type

## Bug Fixes

- Fix the bug where the recorded movie doesn't reflect initial orientation of the device

# 0.13.18 (2016/02/04)

## Bug Fixes

- Fix the bug where Activity.onTouchEvent was interfered by the SDK
- Reduce the possibility of custom events are tracked with invalid timestamp
- Fix potential crashes when stopping recording

# 0.13.15 (2016/01/29)

## Improvements

- Add option to customize the notification icon and its background color
- Remove dependency to Otto
- Add `maskWithRect` API

## Bug Fixes

- Fix WebView event tracking API to support i18n
- Fix crashes when recording floating activity
- Fix crashes while masking
- Fix the recording confirmation dialog duplication

# 0.13.3 (2016/01/15)

## Improvements

- Remove dependency to AWS SDK
- Remove dependency to kotlin-stdlib
- Add option to disable ANDROID_ID collection

## Bug Fixes

- Fixes touch position on floating activity
- Fixes movie concatenation in inproper order

# 0.12.0 (2015/12/18)

## Improvements

- Support Unity (except for recording)

# 0.11.7 (2015/12/15)

## Bug Fixes

- Fixes the bug where the app had been interfered by the SDK listening key events
- Fixes unintentional masking while the target view's parent is GONE

# 0.11.4 (2015/12/12)

## Improvements

- Enables to use large size image for in-app message

## Bug Fixes

- Fixes potential error when building the application with Eclipse
- Fixes the bug where masking feature didn't work correctly

# 0.11.0 (2015/11/30)

## User Profiles

- You can segment the group of users with these profiles when sending push notifications or in-app messages by setting user profiles. [See the doc for more details](http://docs.repro.io/en/api/user-profile.html)

## Improvements

- Supports legacy Play Services SDK
	- You can receive Push Notification with Play Services SDK 3.1.36~. [See the doc for more details](http://docs.repro.io/en/manual/push-notification-android.html)
- Improves memory usage and stability during screen recording

# 0.10.1 (2015/11/3)

## Features

- Supports Eclipse ADT

## Improvements

- Remove dependency to VolleyPlus

# 0.9.3 (2015/10/21)

## Features

- Push notification
- In-app message
- Event tracking for WebView

## Improvements

- Supports older devices
  - Android 2.3~: eligible to install Repro Android SDK with all features disabled
  - Android 4.0~: eligible to install Repro Android SDK except for screen recording
  - Android 4.3~: eligble to install Repro Android SDK with all features available
- Supports Android emulator
  - **Attention:** Screen recording is not supported on Android emulators
- Improves memory management during screen recording

# 0.8.20 (2015/10/01)

- Initial Release
