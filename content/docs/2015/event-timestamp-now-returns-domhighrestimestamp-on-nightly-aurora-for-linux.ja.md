---
title: "Linux 版 Nightly/Aurora で `event.timeStamp` が `DOMHighResTimeStamp` を返すようになりました"
date: "2015-09-09T15:11:00-04:00"
categories: ["dom"]
tags: []
versions: ["43", "45-esr"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1026803"
      title: "Bug 1026803 - Convert native event times to TimeStamps for Linux"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1231619"
      title: "Bug 1231619 - CSS Animation not properly timed when using AngularJS animate on Firefox Developer edition and nightly"
---
バージョン 43 以降、Linux 版の Nightly、Aurora ([Developer Edition](https://www.mozilla.org/firefox/channel/#developer)) 両チャンネルで、[`event.timeStamp`](https://developer.mozilla.org/docs/Web/API/event.timeStamp) プロパティが、従来のミリ秒単位のタイムスタンプに代わり、マイクロ秒単位の [`DOMHighResTimeStamp`](https://developer.mozilla.org/docs/Web/API/DOMHighResTimeStamp) を返すようになりました。この機能は Windows では [Firefox 33](https://www.fxsitecompat.dev/ja/docs/2014/event-timestamp-now-returns-domhighrestimestamp-on-nightly-aurora-for-windows/) 以降実装されていますが、Beta、Release 両チャンネルではまだ無効となっており、OS X ではまだ実装されていません。

**更新**: `DOMHighResTimeStamp` が有効の場合、*AngularJS* のアニメーション機能が正しく動作しないことが報告されています。
