---
title: "`navigator.buildID` will be removed"
date: "2015-10-25T21:43:00-07:00"
categories: ["dom", "privacy-security"]
tags: []
versions: ["future"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=583181"
      title: "Bug 583181 - Don't reveal navigator.buildID to every site on the web"
---
The non-standard [`navigator.buildID`](https://developer.mozilla.org/docs/Web/API/Navigator/buildID) property, that returns the build identifier of Firefox, is considered to be removed to protect user privacy, because the 14-digit identifier data could be used for fingerprinting.
