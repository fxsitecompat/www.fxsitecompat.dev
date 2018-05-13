---
title: "`HTMLTableElement.insertRow` が列を常に `<tbody>` へ挿入するようになりました"
date: "2014-06-09T02:46:54-04:00"
categories: ["dom"]
tags: []
versions: ["32"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1003539"
      title: "Bug 1003539 – HTMLTableElement.insertRow doesn\'t insert the row at the right place when table has a thead or tfoot, no tbody, and no rows"
---
[`HTMLTableElement.insertRow`](https://developer.mozilla.org/docs/Web/API/HTMLTableElement.insertRow) メソッドの挙動が最新の HTML5 仕様に合わせて変更されました。[`<thead>`](https://developer.mozilla.org/docs/Web/HTML/Element/thead) がある一方で [`<tbody>`](https://developer.mozilla.org/docs/Web/HTML/Element/tbody) と [`<tr>`](https://developer.mozilla.org/docs/Web/HTML/Element/tr) が存在しない場合、新しい `<tr>` は既存の `<thead>` ではなく新たに生成された `<tbody>` へ挿入されるようになります。
