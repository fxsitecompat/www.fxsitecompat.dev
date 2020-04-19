---
title: "`<table>` のサイズと位置が `<caption>` を計算に入れるようになりました"
date: "2018-09-06T03:18:00-04:00"
categories: ["css", "dom"]
tags: []
releases: ["63", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=820891"
      title: "Bug 820891 - Table's caption element not taken into account for table's offsetTop and offsetHeight values"
---
従来、`<table>` 要素の `offset*`、`client*`、`scroll*` プロパティ値は `<caption>` 子要素上のそれらの値を除外していました。つまり、`<thead>`、`<tbody>`、`<tfoot>` だけが計算に含まれていました。例えば、`<caption>` の `clientHeight` が `20` で `<tbody>` の `clientHeight` が `80` だった場合、`<table>` の `clientHeight` は `100` ではなく `80` となっていました。

Firefox 63 で現行の CSSOM 仕様と他のブラウザーの挙動に合わせてこの実装が更新されたことで、この例の結果は `100` となります。既存のコードで期待した値を算出するため Firefox 向けに特別な処理を行っていた場合、この変更が影響を及ぼす可能性があります。
