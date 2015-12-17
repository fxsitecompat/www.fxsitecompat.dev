---
title: "Geolocation API is not working on Firefox 43 and later"
date: "2015-12-17T16:05:00-05:00"
categories: ["misc"]
tags: []
versions: ["43", "44", "45", "46"]
statuses: "regressed"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1232995": "Bug 1232995 - HTML5 Geolocation Not Working After Update to version 43"
---
Currently the [Geolocation API](https://developer.mozilla.org/en-US/docs/Web/API/Geolocation) is not working on Firefox 43 and later due to Mozilla's new Google Location Service API key and its rate limit. Both Mozilla and Google are aware of the issue and it will be solved soon.
