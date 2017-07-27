---
title: "Archive API has been disabled"
date: "2014-03-21T04:50:04-04:00"
categories: ["dom"]
tags: []
versions: ["30"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=968883"
      title: "Bug 968883 – ArchiveReader and ArchiveRequest should not be exposed interfaces"
---
The [Archive API](https://hacks.mozilla.org/2012/10/archiveapi-read-out-archive-file-contents-introducing-bleeding-edge/), experimentally implemented since Firefox 17 as [`ArchiveReader`](https://developer.mozilla.org/en-US/docs/Web/API/ArchiveReader) and [`ArchiveRequest`](https://developer.mozilla.org/en-US/docs/Web/API/ArchiveRequest), has been disabled behind a preference. If you'd like to test the API, change the value of `dom.archivereader.enabled` to `true`.
