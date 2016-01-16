---
title: "URLs in an app manifest are now resolved against the manifest URL instead of the origin"
date: "2014-09-01T22:12:15-04:00"
categories: ["dom"]
tags: []
versions: ["34"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1042881": "Bug 1042881 – Resolve manifest properties urls against the manifest url instead of the origin."
---
URLs specified in [Open Web App manifest](https://developer.mozilla.org/en-US/Apps/Build/Manifest) fields are now resolved against the manifest file's URL instead of the app origin. This change enables multiple apps to be installed from the [same origin](https://developer.mozilla.org/en-US/docs/Web/Security/Same-origin_policy).
