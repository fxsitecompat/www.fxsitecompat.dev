---
title: "`jar` protocol support has been disabled by default"
date: "2015-11-04T13:03:00-08:00"
categories: ["networking", "privacy-security"]
tags: []
versions: ["45"]
statuses: "reverted"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1215235"
      title: "Bug 1215235 - Drop support for jar: URIs by default"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1329336"
      title: "Bug 1329336 - Disable loading remote jars by default"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/CFd4w8GzdEI/discussion"
      title: "Intent to unship: jar: URIs from content"
aliases:
    - "/docs/2015/jar-protocol-support-will-be-removed/"
---
The `jar` protocol, that allows to directly link to a file in ZIP archives, is no longer available from Web content due to [security concerns](https://developer.mozilla.org/en-US/docs/Mozilla/Security/Security_and_the_jar_protocol). No other browsers support this Java archive protocol so far.

To enable the `jar` support for any reason on Firefox 45 and later, flip the `network.jar.block-remote-files` preference value to `false`. Otherwise, loading the `jar` protocol will lead to the `NS_ERROR_UNSAFE_CONTENT_TYPE` exception.

**Update**: Since [*IBM iNotes* is broken](https://bugzilla.mozilla.org/show_bug.cgi?id=1255139) due to this change, the `jar` protocol support has been temporarily restored with Firefox 45.0.1. On Firefox Nightly and Developer Edition, the `network.jar.block-remote-files` preference will remain `true`.

**Update 2**: The *iNotes* issue has been fixed with [IBM Notes/Domino 9.0.1 Fix pack 6](http://www-10.lotus.com/ldd/fixlist.nsf/8d1c0550e6242b69852570c900549a74/e413ea1ca447b3bf85257f77006b7f60) released in May 2016.

**Update 3**: Given that *iNotes* no longer relies on the `jar` support, Mozilla is planning to make it disabled again. Firefox 52 [Extended Support Release](https://www.mozilla.org/en-US/firefox/organizations/) (ESR) for organizations won't be affected by this change, so the older versions of *iNotes*, if any, can still be used on the ESR until May 2018.

**Update 4**: The JAR support has been disabled again with [Firefox 55](https://www.fxsitecompat.com/en-CA/docs/2015/jar-protocol-support-has-been-disabled-by-default/).
