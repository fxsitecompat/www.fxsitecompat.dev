---
title: "存在しないオプションが動的に選択された場合に `<select>` の値が正しく更新されるようになりました"
date: "2016-04-24T08:25:00-04:00"
categories: ["dom"]
tags: []
versions: ["46", "52-esr"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1203668"
      title: "Bug 1203668 - changing the value of a select to a value that matches none of the options should put it in a \"no option selected\" state even when it's a combobox (size=1)"
---
従来、JavaScript を使って [`<select>`](https://developer.mozilla.org/docs/Web/HTML/Element/select) 要素の `value` プロパティをどの [`<option>`](https://developer.mozilla.org/docs/Web/HTML/Element/option) にも一致しない値に変更しても、その `<select>` 要素がコンボボックスとして表示されていた場合は、選択状態が適切に更新されていませんでした。

Firefox 46 は HTML 仕様に従ってこのバグを修正し、そうした場合、いずれかの `<option>` が選択されていればその選択を解除するようにしました。つまり、`<select>` 要素の `selectedIndex`、`selectedOptions`、`value` プロパティはそれぞれ `-1`、空白の `HTMLCollection`、空白文字列となります。

新しい挙動は他のブラウザーと同じになるはずですが、Firefox 固有のコードを使っている特定のサイトはこの変更による影響を受ける可能性があります。
