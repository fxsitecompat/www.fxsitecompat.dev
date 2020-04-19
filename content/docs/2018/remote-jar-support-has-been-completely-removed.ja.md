---
title: "リモート JAR 対応が完全に廃止されました"
date: "2018-04-09T16:12:00-04:00"
categories: ["networking", "privacy-security"]
tags: []
versions: ["61", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1427726"
      title: "Bug 1427726 - Remove remote jar support (currently behind a disabled about:config pref)"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/j4z4-iV5IwI/discussion"
      title: "Intent to unship: remote jar: protocol pref"
---
リモート Java アーカイブ (JAR) ファイルの読み込み対応が Firefox 61 でついに削除されました。これは [Firefox 55 以降初期設定で無効化](https://www.fxsitecompat.dev/ja/docs/2017/remote-jar-support-has-been-disabled-again/) されていたものの、必要に応じてブラウザーの隠し設定を使って有効化することが可能でした。

JAR に依存していたことが判明している唯一のウェブアプリケーションである *IBM iNotes* は [2016 年 5 月に更新され](https://www-10.lotus.com/ldd/fixlist.nsf/8d1c0550e6242b69852570c900549a74/e413ea1ca447b3bf85257f77006b7f60)、Firefox での JAR コンポーネントの使用を中止しています。他にどのブラウザーも JAR に対応していないことから、現時点で互換性リスクは非常に低いはずです。
