---
title: "`File.lastModifiedDate` が廃止予定となりました"
date: "2016-06-01T17:16:00-04:00"
categories: ["dom"]
tags: []
versions: ["49"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1048291"
      title: "Bug 1048291 - Remove/Deprecate File::lastModifiedDate"
---
[`File.prototype.lastModifiedDate`](https://developer.mozilla.org/ja/docs/Web/API/File/lastModifiedDate) プロパティは廃止予定なり、将来的に削除されることとなりました。代わりに `lastModified` プロパティを使用してください。
