---
title: "`X-Content-Type-Options: nosniff` now applies to top-level documents, causing some pages to be downloaded"
date: "2019-10-21T19:11:00-04:00"
categories: ["networking", "privacy-security"]
tags: []
versions: ["71"]
statuses: "reverted"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1580607"
      title: "Bug 1580607 - Logout from Office365 causes download dialog box"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1582671"
      title: "Bug 1582671 - Firefox Treats Arris Modem Webpages (application/x-unknown-content-type) As Files to Download"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1587448"
      title: "Bug 1587448 - Enable XTCO-nosniff for FF 71"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1592651"
      title: "Bug 1592651 - Disable Pref respect_document_nosniff for Firefox 71"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1591932"
      title: "Bug 1591932 - Enable Content-Type Sniffing when no Type is provided and Xtco-Nosniff is set"
---
The [`X-Content-Type-Options`](https://developer.mozilla.org/docs/Web/HTTP/Headers/X-Content-Type-Options) HTTP response header has been supported since Firefox 50, and the `nosniff` directive can be used to effectively block scripts and stylesheets served with a wrong MIME type.

Starting with Firefox 71, it will be applied to top-level documents as well, aiming at further improving the browser security. It means HTML web pages served with a MIME type other than `text/html` will be downloaded instead of being rendered when the `X-Content-Type-Options` header is utilized.

There are a couple of sites known to be affected by this change, including *Microsoft Office 365*, so make sure to double check your site.

**Update**: The change has been backed out from Firefox 71. Mozilla developers are planning to redo this in Firefox 72 with some tweaks.
