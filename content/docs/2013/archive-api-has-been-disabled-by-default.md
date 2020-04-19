---
title: "Archive API has been disabled by default"
date: "2013-01-03T03:50:54-05:00"
categories: ["dom"]
tags: []
releases: ["17"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=795930"
      title: "Bug 795930 – ArchiveReader should live behind a pref"
---
The [Archive API](https://hacks.mozilla.org/2012/10/archiveapi-read-out-archive-file-contents-introducing-bleeding-edge/), experimentally implemented in Firefox 17 as [`ArchiveReader`](https://developer.mozilla.org/docs/Web/API/ArchiveReader) and [`ArchiveRequest`](https://developer.mozilla.org/docs/Web/API/ArchiveRequest), was accidentally landed without a prefix. The spec of this API has not been completed yet and it's unstable, therefore it has been disabled with a preference. If you'd like to test the API, change the value of `dom.archivereader.enabled` to `true`.
