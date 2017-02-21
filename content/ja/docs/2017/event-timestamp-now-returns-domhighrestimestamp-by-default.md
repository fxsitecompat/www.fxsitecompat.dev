---
title: "`event.timeStamp` が初期設定で `DOMHighResTimeStamp` を返すようになりました"
date: "2017-02-20T23:45:00-05:00"
categories: ["dom"]
tags: []
versions: ["54"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1026804"
      title: "Bug 1026804 - Make Event.timeStamp return a DOMHighResTimeStamp by default (switch on pref)"
    - url: "https://groups.google.com/forum/#!topic/mozilla.dev.platform/o1LT02foznI"
      title: "Intent to ship: Event.timeStamp as DOMHighResTimeStamp"
---
Firefox 54 以降、すべての Firefox チャンネルおよびプラットフォーム上で、[`Event.prototype.timeStamp`](https://developer.mozilla.org/ja/docs/Web/API/Event/timeStamp) プロパティは、エポック時間からのミリ秒単位でしかなかった整数型 [`DOMTimeStamp`](https://developer.mozilla.org/ja/docs/Web/API/DOMTimeStamp) 値に代わり、整数部にミリ秒、小数部にマイクロ秒を含む、[ページ読み込み](https://developer.mozilla.org/ja/docs/Web/API/PerformanceTiming/navigationStart) からの浮動小数点数型 [`DOMHighResTimeStamp`](https://developer.mozilla.org/ja/docs/Web/API/DOMHighResTimeStamp) 値を返します。

この変更は、[Windows](https://www.fxsitecompat.com/ja/docs/2014/event-timestamp-now-returns-domhighrestimestamp-on-nightly-aurora-for-windows/)、[Linux](https://www.fxsitecompat.com/ja/docs/2015/event-timestamp-now-returns-domhighrestimestamp-on-nightly-aurora-for-linux/)、[macOS](https://bugzilla.mozilla.org/show_bug.cgi?id=1256562) 版の [Firefox Nightly と Developer Edition](https://www.mozilla.org/ja/firefox/channel/desktop/) では既に行われています。Android での実装が完了したことから、Beta、Release 両チャンネルでも初期設定で高精度タイムスタンプが有効となります。

Google Chrome では 2016 年 3 月公開の [Chrome 49](https://developers.google.com/web/updates/2016/01/high-res-timestamps) 以降有効になっていることから、現時点での互換性リスクは低いものと思われます。
