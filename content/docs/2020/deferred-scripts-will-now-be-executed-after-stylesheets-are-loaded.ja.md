---
title: "遅延スクリプトがスタイルシートの読み込み後に実行されるようになりました"
date: "2020-04-06T23:15:00-04:00"
categories: ["css", "html", "javascript"]
tags: []
releases: ["76"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1622235"
      title: "Bug 1622235 - <script defer> should wait for stylesheet loads."
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/VXlDBa3SvWA/discussion"
      title: "Intent to prototype and ship: Make <script defer> wait for stylesheet loads."
---
WHATWG コミュニティにおいて `<script defer>` の一貫性のない挙動について [議論](https://github.com/whatwg/html/issues/3890) が行われ、仕様によればスタイルシートの読み込みを待つべきのところ、旧バージョンの Microsoft Edge 以外のブラウザーはそれに従っていないという状況が指摘されました。この問題は特に Firefox では様々なウェブサイトで [スタイル未指定コンテンツのちらつき](https://en.wikipedia.org/wiki/Flash_of_unstyled_content) (FOUC) を引き起こしていました。

Firefox 76 が問題に対処したことで、標準で遅延処理されるモジュールを含め、遅延スクリプトはすべてのスタイルシートが読み込まれた後で実行されるようになります。ウェブ開発者の皆さんは、他のモダンブラウザーにもこの変更が実装されるまで、レンダリング挙動に一貫性がない可能性を頭に置く必要があります。
