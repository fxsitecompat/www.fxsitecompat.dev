---
title: "`-moz` 接頭辞付き CSS グラデーション内で非標準の複雑な構文が使用できなくなりました"
date: "2019-06-09T21:50:00-04:00"
categories: ["css"]
tags: []
versions: ["68"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1547939"
      title: "Bug 1547939 - Consider simplifying -moz-linear-gradient parsing"
---
Firefox 開発者は後方互換性のため `-moz` 接頭辞付き CSS グラデーションへの対応を廃止しない方針を決定しましたが、Firefox 68 でパーサーが簡素化され、`-moz-linear-gradient`、`-moz-radial-gradient`、`-moz-repeating-linear-gradient` の各関数は標準関数のエイリアスにより近くなりました。

角度と位置の両方を伴った旧来の複雑な構文は今後解析されません。以下は [パッチ](https://hg.mozilla.org/mozilla-central/rev/a484a2625d18) に含まれているいくつかの例です。

```css
-moz-linear-gradient(20% bottom, red, blue);
-moz-radial-gradient(top left 45deg, red, blue);
-moz-repeating-linear-gradient(30grad left 35px, red, blue);
```

一方、WebKit 互換性のため、このように `to` キーワードが抜けている非標準構文への対応は引き続き行われます。

```css
-moz-linear-gradient(top, red, blue); /* 本来は `to top` */
```

ウェブ開発者の皆さんには今後も、既に幅広く対応が行われているこれらの CSS 関数の接頭辞なしバージョンを使用するよう推奨します。
