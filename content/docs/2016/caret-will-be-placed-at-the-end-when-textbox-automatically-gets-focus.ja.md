---
title: "テキストボックスに自動でフォーカスが当たったとき、キャレットが末尾に置かれるようになります"
date: "2016-09-16T00:43:00-04:00"
categories: ["dom"]
tags: []
releases: ["51", "52-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1287655"
      title: "Bug 1287655 - input/textarea selectionStart, selectionEnd should return cursor position when selection is empty"
---
従来、[`focus`](https://developer.mozilla.org/docs/Web/API/HTMLElement/focus) メソッドで `<input>` あるいは `<textarea>` 要素にフォーカスが当たったとき、キャレットは当初テキストの先頭に置かれ、そのためそのフォームコントロール上の `selectionStart`、`selectionEnd` 両プロパティは常に `0` となっていました。

Firefox 51 で HTML 仕様に従ってこの挙動が変更され、キャレットはテキストの末尾に置かれ、それらのプロパティはテキスト長と同じ値になります。必要であれば [`setSelectionRange`](https://developer.mozilla.org/docs/Web/API/HTMLInputElement/setSelectionRange) メソッドを使って選択範囲を指定することが可能です。
