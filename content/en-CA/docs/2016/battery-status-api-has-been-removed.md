---
title: "Battery Status API has been removed"
date: "2016-10-28T23:57:00-04:00"
categories: ["dom", "privacy-security"]
tags: []
versions: ["52"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1313580"
      title: "Bug 1313580 - Remove web content access to Battery API"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/5U8NHoUY-1k/discussion"
      title: "Removing the Battery Status API?"
---
As of Firefox 52, the [Battery Status API](https://developer.mozilla.org/en-US/docs/Web/API/Battery_Status_API) is no longer available from Web content for privacy reasons, where it could be used by remote trackers for user fingerprinting. It's unknown if there were legitimate use cases of the API.
