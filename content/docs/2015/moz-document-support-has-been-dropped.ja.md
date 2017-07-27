---
title: "`@-moz-document` 対応が打ち切られました"
date: "2015-10-13T13:17:00-04:00"
categories: ["css", "privacy-security"]
tags: []
versions: ["future"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1035091"
      title: "Bug 1035091 - limit @-moz-document to user and UA sheets (Makes it useless for exfiltration in CSS-injection attacks)"
---
[`@-moz-document`](https://developer.mozilla.org/ja/docs/Web/CSS/@document) ルールがウェブコンテンツから使用できなくなりました。これは、第三者サイトの URL に含まれる機密データを盗み出す目的で、攻撃者による CSS インジェクションに悪用される恐れがあったためです。Firefox ユーザーは引き続きユーザースタイルシート内でこのルールを使い、ブラウジング体験をパーソナライズすることが可能です。

**更新**: このドキュメントの初期草稿では Firefox 44 で変更が行われたと記載していましたが、`<fieldset>` 要素上の [レイアウト互換性問題](https://bugzilla.mozilla.org/show_bug.cgi?id=504622) のため、パッチはそのバージョンへ投入されませんでした。このバグはまもなく解決する見込みです。
