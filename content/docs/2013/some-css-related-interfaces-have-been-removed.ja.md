---
title: "一部の CSS 関連インターフェイスが削除されました"
date: "2013-10-08T20:15:35-04:00"
categories: ["dom"]
tags: []
versions: ["27"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=872934"
      title: "Bug 872934 – convert style sheet change event interfaces to Web IDL and stick [NoInterfaceObject] on them"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=916871"
      title: "Bug 916871 – Remove classinfo bits for CSSGroupRuleRuleList"
---
グローバルオブジェクトを標準化する現在進行中の取り組みの一環として、非標準のスタイルシート変更イベントインターフェイスである `StyleRuleChangeEvent`、`StyleSheetApplicableStateChangeEvent`、`StyleSheetChangeEvent`がウェブコンテンツから利用できなくなりました。[`CSSRuleList`](https://developer.mozilla.org/docs/Web/API/CSSRuleList) の実装詳細である `CSSGroupRuleRuleList` インターフェイスも削除されました。
