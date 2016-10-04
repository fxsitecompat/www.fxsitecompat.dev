---
title: "`jar` プロトコル対応が初期設定で無効化されました"
date: "2015-11-04T13:03:00-08:00"
categories: ["networking", "privacy-security"]
tags: []
versions: ["45"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1215235"
      title: "Bug 1215235 - Drop support for jar: URIs by default"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/CFd4w8GzdEI/discussion"
      title: "Intent to unship: jar: URIs from content"
aliases:
    - "/docs/2015/jar-protocol-support-will-be-removed/"
---
ZIP アーカイブに含まれるファイルへの直接リンクを可能にする `jar` プロトコルが、[セキュリティ上の懸念](https://developer.mozilla.org/ja/docs/Mozilla/Security/Security_and_the_jar_protocol) から Web コンテンツから使用できなくなりました。他のどのブラウザも今のところこの Java アーカイブプロトコルに対応していません。

何らかの理由で Firefox 45 以降でも `jar` 対応を有効化したい場合は、`network.jar.block-remote-files` の設定値を `false` に切り替えてください。そうしない場合、`jar` プロトコルの読み込みは `NS_ERROR_UNSAFE_CONTENT_TYPE` の例外となります。

**更新**: この変更により [*IBM iNotes* が動作しなくなった](https://bugzilla.mozilla.org/show_bug.cgi?id=1255139) ため、`jar` プロトコル対応は Firefox 45.0.1 で一時的に元に戻されました。Firefox Nightly および Developer Edition では、`network.jar.block-remote-files` の設定は `true` のままとなります。
