---
title: "Windows 版 Nightly/Aurora で `event.timeStamp` が `DOMHighResTimeStamp` を返すようになりました"
date: "2014-07-22T05:06:26-04:00"
categories: ["dom"]
tags: []
versions: "33"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1022396": "Bug 1022396 – Make Event.timeStamp return a DOMHighResTimeStamp on Windows (was Event.timeStamp should be relative to 1st January 1970 rather than the system start)"
---
Windows 版の [Nightly](http://nightly.mozilla.org/)、[Aurora](http://aurora.mozilla.org/) チャンネルで、[`event.timeStamp`](https://developer.mozilla.org/ja/docs/Web/API/event.timeStamp) プロパティが、従来のミリ秒単位のタイムスタンプに代わり、マイクロ秒単位の [`DOMHighResTimeStamp`](https://developer.mozilla.org/ja/docs/Web/API/DOMHighResTimeStamp) を返すようになりました。この機能は Beta、Release チャンネルではまだ無効となっており、[他のプラットフォームでは実装されていません](https://bugzilla.mozilla.org/show_bug.cgi?id=1026803)。
