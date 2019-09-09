---
title: "`line-height:normal` の解析値がピクセルではなく `normal` となりました"
date: "2019-09-09T13:35:00-04:00"
categories: ["css", "dom"]
tags: []
versions: ["71"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1536871"
      title: "Bug 1536871 - Return the keyword value for line-height: normal in getComputedStyle."
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1579624"
      title: "Bug 1579624 - Turn the \"line-height computes as normal\" pref on for release users."
---
Firefox 71 以降、`line-height` CSS プロパティの [解析値](https://developer.mozilla.org/docs/Web/CSS/resolved_value) が、指定値が `normal` あるいは未定義の場合、実際の長さではなく `normal` となります。

```js
// これは今後ピクセルの代わりに `normal` を返す可能性があります
window.getComputedStyle(element).getPropertyValue('line-height');
```

この変更は、CSS Working Group での [議論](https://github.com/w3c/csswg-drafts/issues/3749) を受けて、既に Firefox 69 以降 Nightly と早期 Beta チャンネルで行われていますが、Mozilla の開発者は今のところ互換性問題の報告を目にしていません。新しい挙動は Google Chrome と一致します。Safari も近く同様の変更を行う予定です。
