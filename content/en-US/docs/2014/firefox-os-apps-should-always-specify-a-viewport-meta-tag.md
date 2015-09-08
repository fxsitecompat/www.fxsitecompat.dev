---
title: "Firefox OS apps should always specify a viewport `<meta>` tag"
date: "2014-03-21T04:50:04-04:00"
categories: ["dom"]
tags: []
versions: "30"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=845690": "Bug 845690 – Support meta viewport in Firefox OS apps"
---
[Firefox OS 1.3](https://developer.mozilla.org/en-US/Firefox_OS/Releases/1.3), based on Firefox 28, added the support for a [viewport `<meta>` tag](https://developer.mozilla.org/en-US/docs/Mozilla/Mobile/Viewport_meta_tag) in applications. The default viewport `"width=device-width, height=device-height, user-scalable=no"` will be applied to apps that don't specify one. This implementation is only for backward compatibility and will eventually be removed. [Open Web App](https://developer.mozilla.org/en-US/Apps/Quickstart/Build/Intro_to_open_web_apps) developers are encouraged to always declare a viewport `<meta>` tag to avoid a possible breakage in the future.
