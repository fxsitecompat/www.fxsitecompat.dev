---
title: "`navigator.doNotTrack` が正しい値を返すようになりました"
date: "2014-06-09T02:46:54-04:00"
categories: ["dom"]
tags: []
versions: ["32"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=887703"
      title: "Bug 887703 – Do not track settings results in wrong value for navigator.doNotTrack"
---
これまで、[`navigator.doNotTrack`](https://developer.mozilla.org/ja/docs/Web/API/navigator.doNotTrack) プロパティは、[Do Not Track](http://www.mozilla.org/ja/dnt/) オプションがユーザーによって無効化されている場合でも誤って `"yes"` を返していました。Firefox 32 以降は、仕様に従って `"0"` (無効)、`"1"` (有効) あるいは `"unspecified"` (未設定) を返すようになります。
