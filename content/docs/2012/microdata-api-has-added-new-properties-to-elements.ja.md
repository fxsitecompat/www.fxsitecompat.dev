---
title: "Microdata API によって新たなプロパティが要素に追加されました"
date: "2012-10-15T06:00:00-04:00"
categories: ["dom"]
tags: []
versions: ["16"]
statuses: "affecting"
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=591467"
      title: "Bug 591467 – Implement HTML Microdata API"
---
HTML5 の [Microdata DOM API](http://www.w3.org/TR/microdata/#microdata-dom-api) が実装され、[`Document`](https://developer.mozilla.org/ja/docs/Web/API/Document) インターフェイスに `getItems` プロパティが、[`Element`](https://developer.mozilla.org/ja/docs/Web/API/Element) インターフェイスに `itemId`、`itemProp`、`itemRef`、`itemScope`、`itemType`、`itemValue`、`properties` プロパティがそれぞれ追加されました。

Six Apart の *Movable Type* がこの変更による影響を受けたことが確認されています。独自の `itemId` プロパティが原因で一部機能が正常に動作しなくなったため、同社が [問題を修正](https://github.com/movabletype/movabletype/commit/83d2f3d21d9c9a951d7e872d70bac5d355bd3d4d) し [パッチを公開](http://www.movabletype.jp/faq/firefox-16-patches.html) しています。

各要素に独自データを付加したい場合は、任意のプロパティの代わりに [`HTMLElement.dataset`](https://developer.mozilla.org/ja/docs/Web/API/HTMLElement/dataset) プロパティを使う方が安全でしょう。Firefox には文字列型以外のデータも保存できる [`setUserData`](https://developer.mozilla.org/ja/docs/Web/API/Node/setUserData)、[`getUserData`](https://developer.mozilla.org/ja/docs/Web/API/Node/getUserData) メソッドも実装されています。ただし、これらのメソッドは [`WeakMap`](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/WeakMap) に置き換えられる形で [廃止予定となっています](https://bugzilla.mozilla.org/show_bug.cgi?id=749981)。

**更新**: Microdata API 対応は [Firefox 49 で削除されました](https://www.fxsitecompat.com/ja/docs/2016/microdata-api-has-been-removed/)。
