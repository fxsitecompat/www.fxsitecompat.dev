---
title: "不正な `list-style-type` が順序なしではなく順序付きリストとして表示されるようになりました"
date: "2014-07-22T05:06:26-04:00"
categories: ["css"]
tags: []
versions: ["33"]
statuses: "affected"
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1027647"
      title: "Bug 1027647 – invalid list-style-type makes ordered list from unordered list"
---
Firefox 33 以降、`non`、`bulleted`、`disk` といった不正な [`list-style-type`](https://developer.mozilla.org/ja/docs/Web/CSS/list-style-type) プロパティの値が、`disc` ではなく `decimal` にフォールバックされるようになりました。これは CSS3 Counter Styles 仕様に準拠するための変更です。
