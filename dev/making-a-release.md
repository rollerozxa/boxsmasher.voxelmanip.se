---
title: Making a release
---

This page contains notes for the process of making new releases of Box Smasher.

<!--more-->

## Preparation
Do some reasonably thorough testing of the game beforehand. There should be no crashes, obviously.

Test the game both on desktop as well as on phone to make sure everything looks and feels right there.

## Update version information
Most version information is controlled by the `data/version.json` file. Update this for the new release.

## Packaging
Do the packaging.

```
./packaging/make-all.sh
```

Test so that the resulting builds in bin/ work. Then publish to itch.io:

```
./packaging/publish-itch.sh
```

Check so that everything looks right on the [itch.io page](https://rollerozxa.itch.io/box-smasher).

Make a release on the [rollerozxa/boxsmasher](https://github.com/rollerozxa/boxsmasher) repository. Just make it so that a version number is tagged.

## Packaging on Android
Packaging for Android is done in the [rollerozxa/boxsmasher-android](https://github.com/rollerozxa/boxsmasher-android) repository.

For a new release, do the following:

1. Update the game submodule in `app/src/main/`.
1. Update the version information in `app/build.gradle`.
1. Commit changes, let Github CI run.
1. Test the APK that the CI produces, and then publish it to itch.io with the private `publish-android.sh` script.
1. Tag new release on the [rollerozxa/boxsmasher-android](https://github.com/rollerozxa/boxsmasher-android) repository for F-Droid.

## Announcement
Make a new news post on the Box Smasher website and update the download page.

Then copy the news post and add it as a devlog on itch.io, attaching the newly released downloads to the post.
