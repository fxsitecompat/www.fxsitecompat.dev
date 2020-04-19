---
title: "`File.lastModifiedDate` has been removed"
date: "2018-05-04T13:53:00-04:00"
categories: ["dom"]
tags: []
versions: ["61", "68-esr"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1458883"
      title: "Bug 1458883 - Get rid of File.lastModifiedDate"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1481140"
      title: "Bug 1481140 - Firefox 61.0.1 (64 Bit) does not record correct file modification time and date in OneDrive"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/l-WY9qvfUNg/discussion"
      title: "Intent to unship: File.lastModifiedDate"
---
The non-standard [`File.prototype.lastModifiedDate`](https://developer.mozilla.org/docs/Web/API/File/lastModifiedDate) property, [deprecated since Firefox 49](https://www.fxsitecompat.dev/en-CA/docs/2016/file-lastmodifieddate-has-been-deprecated/), has been removed with Firefox 61. According to Mozilla's [Telemetry](https://telemetry.mozilla.org/), it's currently used in 0.01% of the pages. Use the standard [`lastModified`](https://developer.mozilla.org/docs/Web/API/File/lastModified) property instead.

**Update**: *Microsoft OneDrive* is not showing correct file modification dates due to this change.
