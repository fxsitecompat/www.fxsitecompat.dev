---
title: "Remote JAR support has been disabled again"
date: "2017-04-05T08:46:00-04:00"
categories: ["networking", "privacy-security"]
tags: []
versions: ["55"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1255139"
      title: "Bug 1255139 - iNotes not working after upgrade to release 45.0"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1329336"
      title: "Bug 1329336 - Disable loading remote jars by default"
---
For security reasons, Java archive (JAR) files can no longer be loaded from remote locations by default. This change was originally made with [Firefox 45](https://www.fxsitecompat.com/en-CA/docs/2015/jar-protocol-support-has-been-disabled-by-default/) but soon reverted because *IBM iNotes* was broken. The product was then [updated in May 2016](https://www-10.lotus.com/ldd/fixlist.nsf/8d1c0550e6242b69852570c900549a74/e413ea1ca447b3bf85257f77006b7f60) to not use JAR for Firefox, hence the re-attempt with Firefox 55.

*iNotes* customers must install the Fix Pack to solve the compatibility issue. If the instance cannot be updated now for some reason, use Firefox 52 [Extended Support Release](https://www.mozilla.org/en-US/firefox/organizations/) so the remote JAR support is available until <del>Q2</del> <ins>August</ins> 2018.

No other browsers support JAR. No other broken apps are reported so far.

**Update** The remote JAR support has been [completely removed with Firefox 61](https://www.fxsitecompat.com/en-CA/docs/2018/remote-jar-support-has-been-completely-removed/).
