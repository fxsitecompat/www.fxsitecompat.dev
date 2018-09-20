---
title: "`overflow` ショートハンド構文が更新され、2 つの値が入れ替わりました"
date: "2018-08-17T11:57:00-04:00"
categories: ["css"]
tags: []
versions: ["63"]
statuses: "reverted"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1481866"
      title: "Bug 1481866 - swap values of 2-value 'overflow' syntax so block is first and inline is second"
---
[Firefox 61](https://bugzilla.mozilla.org/show_bug.cgi?id=1453148) 以降、CSS [`overflow`](https://developer.mozilla.org/docs/Web/CSS/overflow) プロパティは `overflow-x` と `overflow-y` の両方を受け入れるショートハンドとなっています。CSS Working Group での最近の議論の結果、縦書きモード対応を改善するために、`overflow-block` と `overflow-inline` という新たな [論理プロパティ](https://developer.mozilla.org/docs/Web/CSS/CSS_Logical_Properties) を受け入れるよう構文が更新されました。

これにより、2 つの x/y 値は以下のように入れ替える必要があります。

```css
overflow-x: scroll;
overflow-y: hidden;
/* Firefox 61 と 62 では、これは以下と同じでした */
overflow: scroll hidden;
/* しかし Firefox 63 以降、これは以下のようになります */
overflow: hidden scroll;
```

このショートハンド構文はまだ新しく、今のところ Firefox と [Google Chrome](https://www.chromestatus.com/feature/5090725653905408) の最新版にしか実装されていないことから、互換性リスクは非常に低いはずで、そのために変更が行われました。

本稿執筆時点で、`overflow-block`、`overflow-inline` 両ロングハンドプロパティは未実装です。

**更新**: 値の入れ替えとは異なる後方互換性に配慮した挙動が最新の仕様で提案されたことから、この変更は [ベータ期間中に取り消されました](https://bugzilla.mozilla.org/show_bug.cgi?id=1492567)。
