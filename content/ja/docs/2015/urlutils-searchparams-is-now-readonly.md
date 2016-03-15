---
title: "`URLUtils.searchParams` が読み取り専用となりました"
date: "2015-06-13T15:20:46-04:00"
categories: ["dom"]
tags: []
versions: ["41"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1174731"
      title: "Bug 1174731 - Make searchParams attribute readonly"
---
[`URLUtils.searchParams`](https://developer.mozilla.org/ja/docs/Web/API/URLUtils/searchParams) プロパティが、[`URLSearchParams`](https://developer.mozilla.org/ja/docs/Web/API/URLSearchParams) インタフェースの複雑性を緩和するために読み取り専用となりました。回避策としては、パラメータを [`URLSearchParams.toString`](https://developer.mozilla.org/ja/docs/Web/API/URLSearchParams/toString) で文字列に変換し、その文字列を [`URLUtils.search`](https://developer.mozilla.org/ja/docs/Web/API/URLUtils/search) で割り当てる方法 ([例](https://github.com/bzdeck/bzdeck/commit/c0841f7f0bfe17fac71b606be6b3777049aea6dc)) があります。
