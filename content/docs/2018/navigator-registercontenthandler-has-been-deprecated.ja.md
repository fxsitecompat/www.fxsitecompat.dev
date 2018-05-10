---
title: "`navigator.registerContentHandler()` が廃止予定となりました"
date: "2018-01-06T04:26:00-05:00"
categories: ["dom"]
tags: []
versions: ["59"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1398169"
      title: "Bug 1398169 - Remove registerContentHandler()"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/jeTDLz38_RE/discussion"
      title: "Intent to unship: navigator.registerContentHandler()"
---
ブラウザーへ [フィードリーダーサービスを関連付ける](https://developer.mozilla.org/ja/Firefox/Releases/2/Adding_feed_readers_to_Firefox) ために使うことができた [`navigator.registerContentHandler`](https://developer.mozilla.org/ja/docs/Web/API/Navigator/registerContentHandler) メソッドが廃止予定となり、近い将来削除されることとなりました。Firefox 59 の時点で Nightly と早期 Beta/DevEdition では初期設定で無効化されています。これは HTML 仕様で標準化されていたものの、他のどのブラウザーもこの機能に対応しておらず、Firefox の実装も標準に準拠していませんでした。ウェブフィードの人気が低下していることから、削除に伴うリスクは少ないはずです。

**更新**: このメソッドは [Firefox 62](https://www.fxsitecompat.com/en-CA/docs/2018/navigator-registercontenthandler-has-been-removed/) で削除されました。このドキュメントの初版では Firefox 59 について言及していましたが、その時点では Release チャンネルではまだ使用可能でした。
