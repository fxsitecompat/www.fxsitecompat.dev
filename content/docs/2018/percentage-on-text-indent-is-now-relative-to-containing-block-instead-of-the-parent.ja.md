---
title: "`text-indent` 上のパーセンテージが内包ブロックの親ではなくそのブロックとの相対値になりました"
date: "2018-11-21T17:41:00-05:00"
categories: ["css"]
tags: []
releases: ["65", "68-esr"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1453298"
      title: "Bug 1453298 - percentage text-indent should be relative to the containing block of the text, not the containing block of the block"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1508509"
      title: "Bug 1508509 - text indent isn't hiding text when using %"
---
従来、[`text-indent`](https://developer.mozilla.org/docs/Web/CSS/text-indent) CSS プロパティにパーセンテージ値が用いられた場合、その内包ブロックの親要素のコンテンツ幅に対して解決されていました。つまり、以下の `p` 要素には `20px` ではなく `50px` のインデントが与えられました。

```html
<div style="width: 500px;">
  <p style="width: 200px; text-indent: 10%;">
    Hello World!
  </p>
</div>
```

この奇妙な挙動が最新の CSS 仕様で解決されました。Firefox 65 が Chrome 72 とともに変更を行ったことにより、今後、値は内包ブロック自体の幅に対して解決されます。期待通り `20px` となる上の例のように、従来よりインデントが短くなる場合があるため、あなたのスタイルシートを見直した方が良いかもしれません。実際、*BBC* のホームページが影響を受けていることが判明しています。
