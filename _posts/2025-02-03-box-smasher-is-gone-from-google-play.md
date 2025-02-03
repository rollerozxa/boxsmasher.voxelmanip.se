---
title: Box Smasher is gone from Google Play
---

As of today, Box Smasher is now no longer available on Google Play, as my developer account and all associated apps have been removed by Google. Even if you have downloaded Box Smasher before, trying to go to its app details page on Google Play will simply lead you to a 404 page.

<!--more-->

{% include image.html
	name="404.webp"
	alt="Google Play 404 page - We're sorry, the requested URL was not found on this server." %}

If you have followed the latest updates of the game this likely should not come as a surprise. I have been aware of this deadline for over a year at this point and subsequently deprecated the Google Play version of Box Smasher when the new 1.1.0 version was released. Why I chose to drop my Google Play developer account as a result of their new developer verification policies can be read in more detail [in a post on my personal blog](https://voxelmanip.se/2025/02/01/goodbye-google-play/).

For 1.1.0, I provide an Android version of the game built by me as an APK available for download on itch.io, which you can sideload onto your device. I have also submitted Box Smasher to [F-Droid](https://f-droid.org), which will be available there in a couple days time once it has been approved and the app has been built by F-Droid's buildservers.

If you have the old Google Play version of Box Smasher installed, you will need to uninstall it first before switching to the itch.io builds or the F-Droid builds, as they use a different signing key and Android does not allow installing app updates with mismatching signing keys. The signing key for apps on Google Play is held by Google nowadays and they do not let developers save a copy of it, which you can probably imagine the reasons why they would do so.
