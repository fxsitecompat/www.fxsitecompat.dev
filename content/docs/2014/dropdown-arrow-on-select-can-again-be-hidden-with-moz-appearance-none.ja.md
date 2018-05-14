---
title: "`<select>` 上のドロップダウン矢印が再度 `-moz-appearance:none` で隠せるようになりました"
date: "2014-10-17T22:50:44-04:00"
categories: ["css"]
tags: []
versions: ["35"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=649849"
      title: "Bug 649849 – Make -moz-appearance:none on a combobox remove the dropdown button"
---
[Firefox 30](https://www.fxsitecompat.com/ja/docs/2014/incorrect-padding-implementation-on-select-has-been-fixed/) で [`<select>`](https://developer.mozilla.org/docs/Web/HTML/Element/select) 要素上の `padding` 誤実装が修正されて以来、[`-moz-appearance`](https://developer.mozilla.org/docs/Web/CSS/-moz-appearance)`:none` と [`text-indent`](https://developer.mozilla.org/docs/Web/CSS/text-indent)、[`text-overflow`](https://developer.mozilla.org/docs/Web/CSS/text-overflow) プロパティの組み合わせを使った、コンボボックスのドロップダウン矢印を隠すハックが動作しなくなっていました。多くの開発者からコンボボックスのスタイルを自由に調整したいという要望が寄せられたため、この非標準の挙動が Firefox 35 で復活することになりました。今後は `-webkit-appearance:none` と同じく、単純に `-moz-appearance:none` を使って以前のようにドロップダウン矢印を隠すことができます。
