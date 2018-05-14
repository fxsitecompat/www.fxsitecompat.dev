---
title: "Archive API が無効化されました"
date: "2014-03-21T04:50:04-04:00"
categories: ["dom"]
tags: []
versions: ["30"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=968883"
      title: "Bug 968883 – ArchiveReader and ArchiveRequest should not be exposed interfaces"
---
[`ArchiveReader`](https://developer.mozilla.org/docs/Web/API/ArchiveReader) と [`ArchiveRequest`](https://developer.mozilla.org/docs/Web/API/ArchiveRequest) という形で Firefox 17 以降試験的に実装されている [Archive API](https://hacks.mozilla.org/2012/10/archiveapi-read-out-archive-file-contents-introducing-bleeding-edge/) が設定で無効化されました。この API を試したい場合は `dom.archivereader.enabled` の値を `true` に変更してください。
