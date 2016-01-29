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
