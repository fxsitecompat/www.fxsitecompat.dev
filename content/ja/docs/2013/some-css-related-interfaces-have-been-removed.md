---
title: "一部の CSS 関連インタフェースが削除されました"
date: "2013-10-08T20:15:35-04:00"
categories: ["dom"]
tags: []
versions: "27"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=872934": "Bug 872934 – convert style sheet change event interfaces to Web IDL and stick [NoInterfaceObject] on them"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=916871": "Bug 916871 – Remove classinfo bits for CSSGroupRuleRuleList"
---
グローバルオブジェクトを標準化する現在進行中の取り組みの一環として、非標準のスタイルシート変更イベントインタフェースである `StyleRuleChangeEvent`、`StyleSheetApplicableStateChangeEvent`、`StyleSheetChangeEvent`が Web コンテンツから利用できなくなりました。[`CSSRuleList`](https://developer.mozilla.org/ja/docs/Web/API/CSSRuleList) の実装詳細である `CSSGroupRuleRuleList` インタフェースも削除されました。
