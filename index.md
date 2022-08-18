---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
title: Home
nav_order: 0
---

<img src="https://raw.githubusercontent.com/vauvenal5/yaga/master/fastlane/metadata/android/en-US/images/featureGraphic.svg" alt="Feature Graphic"/>

# What is Nextcloud Yaga?

Nextcloud Yaga is a Nextcloud first gallery app. It aimes to give you the full functionality of a modern gallery app while utilizing your private Nextcloud server as backend.

Please have a look on the [quickstart guide]({{site.baseurl}}/quickstart/) for first steps.

[<img src="https://play.google.com/intl/en_us/badges/images/generic/en_badge_web_generic.png"
    alt="Get it on Google Play"
    height="80"
    width="250">](https://play.google.com/store/apps/details?id=com.github.vauvenal5.yaga){: .text-decoration: none;}
[<img src="https://fdroid.gitlab.io/artwork/badge/get-it-on.png"
    alt="Get it on F-Droid"
    height="80"
    width="250">](https://f-droid.org/packages/com.github.vauvenal5.yaga){: .text-decoration: none;}

# State of the app

{:.breaking}
Started with refactoring for Android 11+ support. 

{:.info}
FDroid release will not be updated for the time being if you need any of the removed features and are still on Android 10 (API Level 29) or lower consider installing from there.

Due to massive changes in how and were apps are allowed to access files in Anroid 11 and higher (API Level 30+), I have started refactoring Nextcloud Yaga towards using the MediaStore API for local access to images. Only exception are files which are contained in the app folder. This is a lot of work and has implications on the existing functionality. For example, the sync flow which was propesed until now does not work any more. Furthermore, SD card handling is currently broken and root mapping is disabled. Root mapping will be eventually replaced by a new feature, regarding SD card support, I am not sure when I will be able to get back to this.

Issues tracking broken or replacement features will be created soon and linked here.

On a positive note, file provider functionality has been repaired.

## Changelog
- targeting Android 12 (API Level 31)
- refactoring to MediaStore API for local file access
- root mapping deprecated: will be refactored in future when full MediaStore API support is implemented
- automatically resetting root mapping to revert back to default app directory
- local move/copy are currently not supported
- local delete is supported but requires user confirmation
- on Android 12 (API 31+) you can assign MANAGE_MEDIA rights to the app to avoid delete confirmation dialog
- SD card support is broken
- file provider for other apps is fixed
- about app dialog was updated to support news

# Feature Set

The following lists provide only a brief overview.

## Features
Allready included in Nextcloud Yaga:
* Browse images on Nextcloud server
* Load images recursively
* Share image with other apps
* Fetch previews
* Fetch images
* Set local mapping directory
* Light/Dark themes
* Local search/filter
* Change View Types
* Intent support for "Select Image" and "Open with"

## Coming soon
Features that are allready on my mind (not necessarily in that order):
* Upload/Move/Delete
* Multiselect for Sharing/Move/Delete
* Video Support
* Remote Search
* Favourite Folders
* Local Albums
