---
title: "TLS 1.0/1.1 support has been removed"
date: "2020-01-08T19:23:00-05:00"
categories: ["networking", "privacy-security"]
tags: []
versions: ["74"]
statuses: "reverted"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1606734"
      title: "Bug 1606734 - Disable TLS 1.0 and 1.1 by default"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1623534"
      title: "Bug 1623534 - Remote pref override to re-enable TLS 1.0"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1623536"
      title: "Bug 1623536 - Re-enable TLS 1.0 in Firefox 75 (Beta)"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1626495"
      title: "Bug 1626495 - Re-enable TLS 1.0 in Firefox 76 and 77 (Release)"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/8EFRYDR3N1c/discussion"
      title: "Intent to unship: TLS 1.0 and TLS 1.1"
    - url: "https://hacks.mozilla.org/2019/05/tls-1-0-and-1-1-removal-update/"
      title: "TLS 1.0 and 1.1 Removal Update - Mozilla Hacks"
---
The support for the [Transport Layer Security](https://developer.mozilla.org/docs/Web/Security/Transport_Layer_Security) (TLS) protocol's version 1.0 and 1.1, deprecated since [Firefox 71](https://www.fxsitecompat.dev/en-CA/docs/2019/tls-1-0-and-1-1-are-now-deprecated-disabled-in-nightly/), has been removed from all the channels as of Firefox 74. All major browsers are going to drop the support for the older versions of TLS in early 2020.

Make sure to enable TLS 1.2 or 1.3 on your web server, otherwise Firefox will show the [Secure Connection Failed](https://support.mozilla.org/kb/secure-connection-failed-firefox-did-not-connect) error page to prevent users from accessing servers not using the newer version. See [this Mozilla Hacks blog post](https://hacks.mozilla.org/2019/05/tls-1-0-and-1-1-removal-update/) for more information.

**Update**: Mozilla is going to temporarily re-enable the TLS 1.0/1.1 support in Firefox 74 and 75 Beta. The preference change will be remotely applied to Firefox 74, which has already been shipped. This is because many people are currently forced to work at home and relying on online tools amid the novel coronavirus (COVID-19) outbreak, but some of critical government sites still don’t support TLS 1.2 yet. Also due to COVID-19, Google has [postponed the release of Chrome 81](https://blog.chromium.org/2020/03/upcoming-chrome-releases.html) that would [remove their TLS 1.0/1.1 support](https://www.chromestatus.com/feature/5759116003770368). We’ll update this note when the situation has changed.

**Update 2**: TLS 1.0/1.1 will remain enabled in Firefox 76 and 77 as the COVID-19 pandemic continues.
