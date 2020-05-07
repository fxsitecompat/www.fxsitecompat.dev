---
title: "Firefox 77 Beta and Developer Edition are out, COVID-19 continues to affect the development"
date: "2020-05-05T22:59:00-04:00"
---
Mozilla shipped [Firefox 77 Beta and Developer Edition](https://www.mozilla.org/firefox/channel/desktop/) today.

Since the COVID-19 pandemic is still creating huge challenges to many businesses and individuals around the world, Firefox developers have avoided including backward-incompatible changes other than [JPEG image auto rotation](https://www.fxsitecompat.dev/en-CA/docs/2020/jpeg-images-are-now-rotated-by-default-according-to-exif-data/), which is known to be affecting *Slack* and other sites, but Google Chrome has the same issue because they have already shipped the same enhancement. Actually the change to the `image-orientation` CSS property has not landed in Firefox 77 at this writing — it will be probably coming to the Beta channel next week.

The [removal of Application Cache storage](https://www.fxsitecompat.dev/en-CA/docs/2020/application-cache-storage-has-been-removed/) was originally planned for Firefox 77 but postponed.

That’s it for Firefox 77.

Speaking of future releases, Firefox 78 will be the next [Extended Support Release](https://support.mozilla.org/kb/choosing-firefox-update-channel) (ESR) for enterprises, so breaking changes will be avoided again. In the coming weeks, we’ll be documenting all the changes postponed due to COVID-19, which are going to be shipped with Firefox 79 or later.

We’re also busy working on the compatibility checker in our [Firefox Developer Tools extension](https://addons.mozilla.org/firefox/addon/site-compatibility-tools/). The CSS support is coming soon. Stay tuned, stay safe!
