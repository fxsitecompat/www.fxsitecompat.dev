---
title: "FTP support will be removed"
date: "2020-04-10T02:21:00-04:00"
categories: ["networking", "privacy-security"]
tags: []
versions: ["future"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1570155"
      title: "Bug 1570155 - How many people use FTP?"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1574475"
      title: "Bug 1574475 - Remove FTP support"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1622409"
      title: "Bug 1622409 - Put FTP code behind a pref"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/FqCZUT9ay_o/discussion"
      title: "Intent to unship: FTP protocol implementation"
---
For security reasons, Mozilla is planning to remove the FTP support from Firefox in 2021. It’s an insecure protocol, and the usage rate is very low at this time (0.05% according to Mozilla). It’s difficult to maintain the very old implementation in Firefox, and there’s no plan to add the support for FTPS.

Starting with Firefox 77, the FTP support will be disabled in the Nightly channel. The protocol will be handled by an external application such as a standalone FTP client or file manager.

Note that [Google](https://www.chromestatus.com/feature/6246151319715840) has also deprecated the FTP support in their Chrome browser. If you’re running a FTP server, it’s time to consider serving files from a Web server over HTTPS, though the concrete deprecation schedule is not yet decided because of the COVID-19 pandemic.
