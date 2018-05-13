---
title: "Certain secure sites are broken due to outdated version of NSS"
date: "2017-01-11T17:12:00-05:00"
categories: ["privacy-security"]
tags: []
versions: ["51"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1317857"
      title: "Bug 1317857 - There are servers using old and broken versions of NSS"
---
Mozilla developers have discovered several secure servers not working on Firefox 51 (and Google Chrome Canary), showing the "[Secure Connection Failed](https://support.mozilla.org/en-US/kb/secure-connection-failed-error-message)" error page. A [list of the broken sites](https://bug1317857.bmoattachments.org/attachment.cgi?id=8811077) can be found in the tracking bug, but there is probably more.

Those servers are apparently using an outdated version of the [Network Security Services](https://developer.mozilla.org/docs/Mozilla/Projects/NSS) (NSS) library which [contains a bug](https://bugzilla.mozilla.org/show_bug.cgi?id=1317857#c13) in the `signature_algorithms` parsing, throws `PR_END_OF_FILE_ERROR` on the latest browsers coming with NSS 3.28 or later, and therefore has to be upgraded to a newer version.
