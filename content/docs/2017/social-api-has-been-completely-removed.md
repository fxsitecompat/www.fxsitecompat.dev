---
title: "Social API has been completely removed"
date: "2017-08-17T11:17:00-04:00"
categories: ["misc"]
tags: []
versions: ["57"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1388902"
      title: "Bug 1388902 - Shut down the last of socialapi"
    - url: "https://mail.mozilla.org/pipermail/firefox-dev/2017-August/005709.html"
      title: "Intent to remove SocialAPI Share"
---
Mozilla's non-standard [Social Share API](https://developer.mozilla.org/docs/Mozilla/Projects/Social_API/Share), that allowed to integrate [social media services](https://activations.cdn.mozilla.net/) with the browser, has been removed with Firefox 57 because of the low usage rate. The most of the [Social API](https://developer.mozilla.org/docs/Mozilla/Projects/Social_API) sets have already been removed with [Firefox 51](https://www.fxsitecompat.com/en-CA/docs/2016/social-api-has-been-removed-except-the-sharing-functionality/) except for the sharing functionality. Service providers are recommended to instead offer a [browser extension](https://developer.mozilla.org/Add-ons/WebExtensions) to encourage user engagement directly from the browser.
