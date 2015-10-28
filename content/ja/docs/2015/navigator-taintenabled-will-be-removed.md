---
title: "`navigator.taintEnabled` が削除されます"
date: "2015-10-27T22:52:00-07:00"
categories: ["dom"]
tags: []
versions: ["future"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=679971": "Bug 679971 - remove Navigator.taintEnabled()"
---
Netscape 由来の [`navigator.taintEnabled`](https://developer.mozilla.org/ja/docs/Web/API/NavigatorID/taintEnabled) メソッドは Firefox では `false` を返すだけですが、多くのサイトでブラウザ判別に使用されているようです。削除された時点でサイトが動作しなくなる可能性がありますので、今後これを使用することは避けてください。
