---
title: "Touch events support has been temporarily disabled on desktop"
date: "2013-05-19T07:35:00-04:00"
categories: [event-handling]
tags: []
versions: "24"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=888304": "Bug 888304 – Content touch-events on Firefox-desktop should be disabled until we can support them properly"
---
The [touch events](https://developer.mozilla.org/en-US/docs/Web/Guide/API/DOM/Events/Touch_events) support introduced with [Firefox 18](https://www.fxsitecompat.com/en-US/versions/18/) has been disabled on the **desktop** version of Firefox, as some popular sites including Google and Twitter are not working properly. Once the bug is fixed, the API will be enabled again. To enable it anyway, open `about:config` and set the `dom.w3c_touch_events.enabled` pref to `2`. The mobile versions including [Firefox for Android](https://developer.mozilla.org/en-US/docs/Mozilla/Firefox_for_Android) and [Firefox OS](https://developer.mozilla.org/en-US/docs/Mozilla/Firefox_OS) are not affected by this change. Also, the API has been enabled on the Metro-style version of Firefox for Windows 8.
