---
title: "`@-moz-document` 対応が打ち切られました"
date: "2015-10-13T13:17:00-04:00"
categories: ["css", "privacy-security"]
tags: []
versions: "44"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1035091": "Bug 1035091 - limit @-moz-document to user and UA sheets (Makes it useless for exfiltration in CSS-injection attacks)"
---
[`@-moz-document`](https://developer.mozilla.org/en-US/docs/Web/CSS/@document) ルールが Web コンテンツから使用できなくなりました。これは、第三者サイトの URL に含まれる機密データを盗み出す目的で、攻撃者による CSS インジェクションに悪用される恐れがあったためです。Firefox ユーザは引き続きユーザスタイルシート内でこのルールを使い、ブラウジング体験をパーソナライズすることが可能です。
