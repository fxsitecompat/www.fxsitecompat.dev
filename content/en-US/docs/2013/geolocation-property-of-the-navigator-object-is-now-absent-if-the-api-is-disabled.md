---
title: "`geolocation` property of the `navigator` object is now absent if the API is disabled"
date: "2013-07-14T19:12:37-04:00"
categories: ["dom"]
tags: []
versions: "25"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=884921": "Bug 884921 – Align navigator.geolocation with spec"
---
The [Geolocation API](https://developer.mozilla.org/en-US/docs/WebAPI/Using_geolocation) implementation has been updated to comply with the spec. If the feature is not available, [`window.navigator.geolocation`](https://developer.mozilla.org/en-US/docs/Web/API/window.navigator.geolocation) will return `undefined` instead of `null`, and `"geolocation" in navigator` will be `false` instead of `true` previously.
