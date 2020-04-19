---
title: "RC4 is no longer supported on Nightly and Developer Edition"
date: "2015-09-23T06:18:00-04:00"
categories: ["privacy-security"]
tags: []
versions: ["42", "45-esr"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1201023"
      title: "Bug 1201023 - Disable fallback whitelist in Nightly/DevEdition"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/JIEFcrGhqSM/discussion"
      title: "Intent to ship: RC4 disabled by default in Firefox 44"
---
Mozilla and other major browser vendors have agreed to stop supporting the insecure RC4 cipher suites, [deprecated since Firefox 36](https://www.fxsitecompat.dev/en-CA/docs/2014/rc4-support-has-been-deprecated/), finally in early <time datetime="2016">2016</time>. As per the [deprecation plan](https://groups.google.com/d/topic/mozilla.dev.platform/JIEFcrGhqSM/discussion), the [whitelist](https://dxr.mozilla.org/mozilla-central/source/security/manager/ssl/IntolerantFallbackList.inc) allowing certain sites to use RC4 has been disabled on Firefox Nightly and Developer Edition.

Starting with Firefox 44, the RC4 support will be disabled by default on all channels. Web servers must be upgraded as soon as possible to use stronger cipher suites.
