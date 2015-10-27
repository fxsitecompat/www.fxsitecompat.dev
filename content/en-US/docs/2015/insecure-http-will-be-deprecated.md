---
title: "Insecure HTTP will be deprecated"
date: "2015-10-27T16:00:00-07:00"
categories: ["networking", "privacy-security"]
tags: []
versions: ["future"]
statuses: "affected"
references:
    "https://groups.google.com/d/topic/mozilla.dev.platform/GDSnSI9inOo/discussion": "Deprecate geolocation and getUserMedia() for unauthenticated origins"
    "https://groups.google.com/d/topic/mozilla.dev.platform/vavZdN4tX44/discussion": "Intent to deprecate: persistent permissions over HTTP"
    "https://groups.google.com/d/topic/mozilla.dev.platform/xaGffxAM-hs/discussion": "Intent to deprecate: Insecure HTTP"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1072859": "Bug 1072859 - Deprecate non-TLS usage of geolocation"
---
There is a broad industrial agreement that Internet connections should always be encrypted. As per Mozilla developers' proposal, several functionalities that need user permission, including [Geolocation](https://developer.mozilla.org/en-US/docs/Web/API/Geolocation/Using_geolocation), [Notification](https://developer.mozilla.org/en-US/docs/Web/API/Notifications_API), [Fullscreen](https://developer.mozilla.org/en-US/docs/Web/API/Fullscreen_API), [Pointer Lock](https://developer.mozilla.org/en-US/docs/Web/API/Pointer_Lock_API) and [Media Stream](https://developer.mozilla.org/en-US/docs/Web/API/Media_Streams_API) APIs, may probably require HTTPS first.

Although there is no solid timeline yet, the deprecation of insecure HTTP will happen in the not-so-distant future. Web publishers are strongly recommended to develop a plan to migrate to HTTPS as soon as possible. To make transitions easier, [Let's Encrypt](https://letsencrypt.org/), a new certificate authority run by Mozilla and others, will give everyone a trusted certificate for free starting from November 2015.

We will update this document based on the most recent status.
