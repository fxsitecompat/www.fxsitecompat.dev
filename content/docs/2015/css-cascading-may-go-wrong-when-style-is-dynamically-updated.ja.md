---
title: "スタイルの動的更新時に CSS カスケーディングがうまくいかない場合があります"
date: "2015-10-04T22:08:00-04:00"
categories: ["css"]
tags: []
releases: ["41"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1209603"
      title: "Bug 1209603 - specific combinations of em units and dynamic style changes can cause incorrect values of font properties"
---
Firefox 41 で強化されたスタイルキャッシュ機構が原因で、CSS カスケーディング効果にバグが発生しました。これは、スタイルが特定の方法でスクリプトによって変更された場合に、プロパティ値が誤って計算されるという問題です。今のところ報告が 1 件しかないことから、この問題が発生する状況は非常に限られているようです。Mozilla 開発者が解決策に取り組んでいます。

**更新**: このバグは、フォントプロパティに関してのみ再現するようでしたが、Firefox 44 で修正されました。
