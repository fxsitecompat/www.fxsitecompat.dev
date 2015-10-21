---
title: "RC4 is now allowed only on whitelisted sites"
date: "2015-09-25T00:54:00-04:00"
categories: ["privacy-security"]
tags: []
versions: ["43"]
statuses: "reverted"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1201024": "Bug 1201024 - Disable unrestricted RC4 fallback"
    "https://groups.google.com/d/topic/mozilla.dev.platform/JIEFcrGhqSM/discussion": "Intent to ship: RC4 disabled by default in Firefox 44"
---
Mozilla and other major browser vendors have agreed to stop supporting the insecure RC4 cipher suites, [deprecated since Firefox 36](https://www.fxsitecompat.com/en-US/docs/2014/rc4-support-has-been-deprecated/), finally in early <time datetime="2016">2016</time>. As per the [deprecation plan](https://groups.google.com/d/topic/mozilla.dev.platform/JIEFcrGhqSM/discussion), the [whitelist](https://dxr.mozilla.org/mozilla-central/source/security/manager/ssl/IntolerantFallbackList.inc) allowing certain sites to use RC4 has been applied to the Beta and Release channels, in addition to Firefox Nightly and Developer Edition. That means users will see the [Untrusted Connection](https://support.mozilla.org/en-US/kb/connection-untrusted-error-message) error message on various non-whitelisted RC4-enabled sites.

Starting with Firefox 44, the RC4 support will be disabled by default on all channels. Web servers must be upgraded as soon as possible to use stronger cipher suites.

**Update**: This change has been [reverted](https://bugzilla.mozilla.org/show_bug.cgi?id=1207257) because the UI that allows temporarily using RC4 is not ready yet.
