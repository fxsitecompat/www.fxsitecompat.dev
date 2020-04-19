---
title: "Remote JAR support has been completely removed"
date: "2018-04-09T16:12:00-04:00"
categories: ["networking", "privacy-security"]
tags: []
versions: ["61", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1427726"
      title: "Bug 1427726 - Remove remote jar support (currently behind a disabled about:config pref)"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/j4z4-iV5IwI/discussion"
      title: "Intent to unship: remote jar: protocol pref"
---
Firefox 61 has finally removed the support for loading remote Java archive (JAR) files, which had been [disabled by default since Firefox 55](https://www.fxsitecompat.dev/en-CA/docs/2017/remote-jar-support-has-been-disabled-again/) but could be enabled using the browser's hidden preference when necessary.

*IBM iNotes*, the only web application known to had relied on JAR, was [updated in May 2016](https://www-10.lotus.com/ldd/fixlist.nsf/8d1c0550e6242b69852570c900549a74/e413ea1ca447b3bf85257f77006b7f60) to stop using JAR components in Firefox. Given that no other browsers support JAR, the compatibility risk should be very low at this time.
