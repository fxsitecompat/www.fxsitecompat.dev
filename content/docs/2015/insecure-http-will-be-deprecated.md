---
title: "Insecure HTTP will be deprecated"
date: "2015-10-27T16:00:00-07:00"
categories: ["networking", "privacy-security"]
tags: []
versions: ["future"]
statuses: "affecting"
references:
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/GDSnSI9inOo/discussion"
      title: "Deprecate geolocation and getUserMedia() for unauthenticated origins"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/vavZdN4tX44/discussion"
      title: "Intent to deprecate: persistent permissions over HTTP"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/xaGffxAM-hs/discussion"
      title: "Intent to deprecate: Insecure HTTP"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1072859"
      title: "Bug 1072859 - Disable Geolocation on non-secure origins"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1160368"
      title: "Bug 1160368 - Treat cookies set over non-secure HTTP as session cookies"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1335740"
      title: "Bug 1335740 - Consider disabling getUserMedia on non-secure origins"
    - url: "https://blog.mozilla.org/security/2018/01/15/secure-contexts-everywhere/"
      title: "Mozilla Security Blog: Secure Contexts Everywhere"
---
There is a broad industrial agreement that Internet connections should always be encrypted. The new [Service Worker API](https://developer.mozilla.org/en-US/docs/Web/API/Service_Worker_API) requires HTTPS from the first. As per Mozilla developers' proposal, several functionalities that need user permission, including the [Geolocation](https://developer.mozilla.org/en-US/docs/Web/API/Geolocation/Using_geolocation), [Notification](https://developer.mozilla.org/en-US/docs/Web/API/Notifications_API), [Fullscreen](https://developer.mozilla.org/en-US/docs/Web/API/Fullscreen_API), [Pointer Lock](https://developer.mozilla.org/en-US/docs/Web/API/Pointer_Lock_API) and [Media Stream](https://developer.mozilla.org/en-US/docs/Web/API/Media_Streams_API) APIs, may also require HTTPS later.

Another proposal is to treat non-HTTPS cookies as session cookies, which could encourage ad networks and publishers to move to HTTPS.

Although there is no solid timeline yet, the deprecation of insecure HTTP will happen in the not-so-distant future. Web publishers are strongly recommended to develop a plan to migrate to HTTPS as soon as possible. To make transitions easier, [Let's Encrypt](https://letsencrypt.org/), a new certificate authority run by Mozilla and others, gives everyone a trusted certificate for free starting from November 2015.

We will update this document based on the most recent status.

**Update**: As of [Firefox 55](https://www.fxsitecompat.com/en-CA/docs/2017/use-of-geolocation-api-is-now-limited-to-secure-sites/), Use of Geolocation API is now limited to secure sites.

**Update 2**: In January 2018, Mozilla announced their intent to [require HTTPS](https://blog.mozilla.org/security/2018/01/15/secure-contexts-everywhere/) for all new features plus some existing features. Starting with [Firefox 60](https://www.fxsitecompat.com/en-CA/docs/2017/webvr-can-no-longer-be-used-on-insecure-sites/), WebVR can no longer be used on insecure sites.
