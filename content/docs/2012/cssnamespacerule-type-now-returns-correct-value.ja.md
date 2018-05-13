---
title: "`CSSNameSpaceRule.type` が正しい値を返すようになりました"
date: "2012-10-09T06:00:00-04:00"
categories: ["dom"]
tags: []
versions: ["16"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=765590"
      title: "Bug 765590 – CSSNameSpaceRule.type should be 10, not 0"
---
[`CSSNamespaceRule`](https://developer.mozilla.org/docs/Web/API/CSSNamespaceRule) インターフェイスの `type` プロパティが、`CSSRule.UNKNOWN_RULE (0)` ではなく `CSSRule.NAMESPACE_RULE (10)` を返すようになりました。
