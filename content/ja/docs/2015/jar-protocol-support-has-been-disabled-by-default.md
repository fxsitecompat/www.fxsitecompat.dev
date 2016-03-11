---
title: "`jar` プロトコル対応が初期設定で無効化されました"
date: "2015-11-04T13:03:00-08:00"
categories: ["networking"]
tags: []
versions: ["45"]
statuses: "affected"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1215235": "Bug 1215235 - Drop support for jar: URIs by default"
    "https://groups.google.com/d/topic/mozilla.dev.platform/CFd4w8GzdEI/discussion": "Intent to unship: jar: URIs from content"
aliases:
    - "/docs/2015/jar-protocol-support-will-be-removed/"
---
ZIP アーカイブに含まれるファイルへの直接リンクを可能にする `jar` プロコトルが Web コンテンツから使用できなくなりました。他のどのブラウザも今のところこの Java アーカイブプロコトルに対応していません。何らかの理由で Firefox 45 以降でも `jar` 対応を有効化したい場合は、`network.jar.block-remote-files` の設定値を切り替えてください。

**更新**: この変更により [*IBM iNotes* が動作しなくなった](https://bugzilla.mozilla.org/show_bug.cgi?id=1255139) ため、`jar` プロトコル対応は Firefox 45.0.1 で一時的に元に戻されます。Firefox Nightly および Developer Edition では、`network.jar.block-remote-files` の設定は `true` のままとなります。
