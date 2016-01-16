---
title: "`X-Content-Duration` header for Ogg media is no longer supported"
date: "2015-09-15T23:38:00-04:00"
categories: ["audio-video", "networking"]
tags: []
versions: ["41"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1160695": "Bug 1160695 - Clean up duration tracking and use mirroring for cross-thread access"
---
The [`X-Content-Duration` HTTP header](https://developer.mozilla.org/en-US/docs/Web/HTTP/Configuring_servers_for_Ogg_media#Serve_X-Content-Duration_headers), that can be used by Web servers to let browsers know the duration of Ogg format media, is no longer supported by Firefox due to the low adoption rate and maintenance cost. Alternatively, Firefox is able to identify the duration without seeking to the end of the stream when a [keyframe index for Ogg media](http://blog.pearce.org.nz/2010/08/keyframe-indexed-ogg-files-supported-in.html) is provided.
