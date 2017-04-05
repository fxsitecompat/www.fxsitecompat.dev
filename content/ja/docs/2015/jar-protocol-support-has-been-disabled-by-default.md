---
title: "`jar` プロトコル対応が初期設定で無効化されました"
date: "2015-11-04T13:03:00-08:00"
categories: ["networking", "privacy-security"]
tags: []
versions: ["45"]
statuses: "reverted"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1215235"
      title: "Bug 1215235 - Drop support for jar: URIs by default"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1329336"
      title: "Bug 1329336 - Disable loading remote jars by default"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/CFd4w8GzdEI/discussion"
      title: "Intent to unship: jar: URIs from content"
aliases:
    - "/docs/2015/jar-protocol-support-will-be-removed/"
---
ZIP アーカイブに含まれるファイルへの直接リンクを可能にする `jar` プロトコルが、[セキュリティ上の懸念](https://developer.mozilla.org/ja/docs/Mozilla/Security/Security_and_the_jar_protocol) からウェブコンテンツから使用できなくなりました。他のどのブラウザーも今のところこの Java アーカイブプロトコルに対応していません。

何らかの理由で Firefox 45 以降でも `jar` 対応を有効化したい場合は、`network.jar.block-remote-files` の設定値を `false` に切り替えてください。そうしない場合、`jar` プロトコルの読み込みは `NS_ERROR_UNSAFE_CONTENT_TYPE` の例外となります。

**更新**: この変更により [*IBM iNotes* が動作しなくなった](https://bugzilla.mozilla.org/show_bug.cgi?id=1255139) ため、`jar` プロトコル対応は Firefox 45.0.1 で一時的に元に戻されました。Firefox Nightly および Developer Edition では、`network.jar.block-remote-files` の設定は `true` のままとなります。

**更新 2**: *iNotes* の問題は 2016 年 5 月公開の [IBM Notes/Domino 9.0.1 Fix pack 6](http://www-10.lotus.com/ldd/fixlist.nsf/8d1c0550e6242b69852570c900549a74/e413ea1ca447b3bf85257f77006b7f60) で修正されました。

**更新 3**: *iNotes* による `jar` 対応依存が解決したことから、Mozilla は再びその無効化を検討しています。法人向けの Firefox 52 [延長サポート版](https://www.mozilla.org/ja/firefox/organizations/) (ESR) はこの変更による影響を受けないため、旧バージョンの *iNotes* がもしある場合は 2018 年 5 月まで ESR 上で使い続けることができます。

**更新 4**: JAR 対応は [Firefox 55](https://www.fxsitecompat.com/ja/docs/2015/jar-protocol-support-has-been-disabled-by-default/) で再度無効化されました。
