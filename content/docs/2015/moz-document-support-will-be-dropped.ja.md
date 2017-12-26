---
title: "`@-moz-document` 対応が打ち切られます"
date: "2015-10-13T13:17:00-04:00"
categories: ["css", "privacy-security"]
tags: []
versions: ["future"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1035091"
      title: "Bug 1035091 - limit @-moz-document to user and UA sheets (Makes it useless for exfiltration in CSS-injection attacks)"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1422245"
      title: "Bug 1422245 - Toggle the pref to disable @-moz-document in content pages on release"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1423331"
      title: "Bug 1423331 - telegram text box cursor is confused when focusing both window and textbox in 59.0a1 (2017-12-05) (64-bit)"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1426068"
      title: "Bug 1426068 - Disabling @-moz-document results in users being unable to enter line-breaks into YouTube comments"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/RysotXvooV0/discussion"
      title: "Intent to unship: @-moz-document from content pages."
aliases:
    - "/ja/docs/2015/moz-document-support-has-been-dropped/"
---
[`@-moz-document`](https://developer.mozilla.org/ja/docs/Web/CSS/@document) ルールがウェブコンテンツから使用できなくなります。これは、第三者サイトの URL に含まれる機密データを盗み出す目的で、攻撃者による CSS インジェクションに悪用される恐れがあったためです。Firefox ユーザーは引き続きユーザースタイルシート内でこのルールを使い、ブラウジング体験をパーソナライズすることが可能です。

**更新**: このドキュメントの初期草稿では Firefox 44 で変更が行われたと記載していましたが、`<fieldset>` 要素上の [レイアウト互換性問題](https://bugzilla.mozilla.org/show_bug.cgi?id=504622) のため、パッチはそのバージョンへ投入されませんでした。このバグはまもなく解決する見込みです。

**更新 2**: この @ 規則対応は Firefox 59 の時点で再び Nightly と早期ベータ版から削除されました。近く完全に廃止されます。

**更新 3**: *Telegram* と *YouTube* がこの変更の影響を受けることが判明しています。
