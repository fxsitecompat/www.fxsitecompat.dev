---
title: "Linux 版 Nightly/Aurora で `event.timeStamp` が `DOMHighResTimeStamp` を返すようになりました"
date: "2015-09-09T15:11:00-04:00"
categories: ["dom"]
tags: []
versions: ["43"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1026803": "Bug 1026803 - Convert native event times to TimeStamps for Linux"
---
バージョン 43 以降、Linux 版の Nightly、Aurora ([Developer Edition](https://www.mozilla.org/firefox/channel/#developer)) 両チャンネルで、[`event.timeStamp`](https://developer.mozilla.org/ja/docs/Web/API/event.timeStamp) プロパティが、従来のミリ秒単位のタイムスタンプに代わり、マイクロ秒単位の [`DOMHighResTimeStamp`](https://developer.mozilla.org/ja/docs/Web/API/DOMHighResTimeStamp) を返すようになりました。この機能は Windows では [Firefox 33](https://www.fxsitecompat.com/ja/docs/2014/event-timestamp-now-returns-domhighrestimestamp-on-nightly-aurora-for-windows/) 以降実装されていますが、Beta、Release 両チャンネルではまだ無効となっており、OS X ではまだ実装されていません。
