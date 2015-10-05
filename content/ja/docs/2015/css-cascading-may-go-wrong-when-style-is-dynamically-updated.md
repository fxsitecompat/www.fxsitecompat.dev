---
title: "スタイルの動的更新時に CSS カスケーディングがうまくいかない場合があります"
date: "2015-10-04T22:08:00-04:00"
categories: ["css"]
tags: []
versions: "41"
statuses: "regressed"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1209603": "Bug 1209603 - bad css cascade in version 41"
---
Firefox 41 で強化されたスタイルキャッシュ機構が原因で、CSS カスケーディング効果にバグが発生しました。これは、スタイルが特定の方法でスクリプトによって変更された場合に、プロパティ値が誤って計算されるという問題です。Mozilla 開発者が解決策に取り組んでいます。
