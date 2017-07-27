---
title: "`DataTransfer.types` が `DOMStringList` から `Array` に変わりました"
date: "2016-12-16T02:13:00-05:00"
categories: ["dom"]
tags: []
versions: ["52"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1298243"
      title: "Bug 1298243 - drag/drop: DataTransfer.types is wrong type"
---
Firefox はこれまで [`DataTransfer.prototype.types`](https://developer.mozilla.org/ja/docs/Web/API/DataTransfer/types) プロパティに [`DOMStringList`](https://developer.mozilla.org/ja/docs/Web/API/DOMStringList) を返していました。Firefox 52 以降では、現行の HTML 仕様に従い、単純な `DOMString` の `Array` を返すようになります。つまり、このプロパティ上で `contains` メソッドは使えなくなり、特定の種類のデータが提供されているかどうかを調べるには、代わりに [`includes`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Array/includes) メソッドを使う必要があります。

後方互換性のため、以下のように [スプレッド構文](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Operators/Spread_operator) を使うことができます。

```js
document.body.addEventListener('drop', event => {
  event.preventDefault();

  if ([...event.dataTransfer.types].includes('text/html')) {
    // 何か処理を実行
  }
});
```

**更新**: *JIRA* での添付ファイルのドラッグ＆ドロップがこの変更により動作しなくなっています。Atlassian は [問題を修正済み](https://bitbucket.org/atlassian/jira-drag-drop-attachments-plugin/commits/3dbc08643607a680339d485877af501c0572e1b1) です。解決策は [こちらのスレッド](https://jira.atlassian.com/browse/JRA-64414) を参照してください。
