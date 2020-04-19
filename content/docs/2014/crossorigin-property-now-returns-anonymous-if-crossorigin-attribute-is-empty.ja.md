---
title: "`crossorigin` 属性が空白の場合に `crossOrigin` プロパティが `anonymous` を返すようになりました"
date: "2014-10-17T22:50:44-04:00"
categories: ["dom"]
tags: []
releases: ["35", "38-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=880997"
      title: "Bug 880997 – Reflect crossOrigin as a limited enumerated attribute"
---
HTML メディア要素の [`crossOrigin`](https://developer.mozilla.org/docs/Web/HTML/CORS_settings_attributes) プロパティが、その要素の `crossorigin` 属性が空白の場合に `"anonymous"` を返すようになりました。この変更は、同じく空文字列を返す属性なしの場合との区別を付けるために行われたものです。
