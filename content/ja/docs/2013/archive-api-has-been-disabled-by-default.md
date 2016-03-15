---
title: "Archive API が初期設定で無効化されました"
date: "2013-01-03T03:50:54-05:00"
categories: ["dom"]
tags: []
versions: ["17"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=795930"
      title: "Bug 795930 – ArchiveReader should live behind a pref"
---
Firefox 17 で `ArchiveReader` と `ArchiveRequest` として試験実装された [Archive API](https://dev.mozilla.jp/2012/08/archive-api-experimental-implement/) は、誤って接頭辞なしで投入されていました。この API は現時点でまだ仕様が完成しておらず不安定なことから、設定によって無効化する変更が行われました。試したい場合は `dom.archivereader.enabled` の値を `true` にする必要があります。
