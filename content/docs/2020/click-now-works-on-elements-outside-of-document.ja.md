---
title: "`click()` が `document` 外の要素上でも動作するようになりました"
date: "2020-02-17T23:48:00-05:00"
categories: ["dom"]
tags: []
releases: ["75"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1610821"
      title: "Bug 1610821 - Ensure click() works on input elements which are disconnected from a document"
---
Firefox はこれまで、`document` に含まれていない要素上で呼び出された [`HTMLElement.click`](https://developer.mozilla.org/docs/Web/API/HTMLElement/click) メソッドを無視していました。Firefox 74 以降、そうしたメソッド呼び出しが動作するようになり、その要素上でそれに伴う `click` イベントが発生します。この新たな挙動は他のブラウザーとほぼ一致するため、サイト互換性問題の原因となる恐れは低いと考えられます。ただ、サイトがユーザーエージェント判別を使用して Firefox 専用のコードを実行しており、それが `click` イベントが発生しないことを前提としていた場合、この変更は潜在的な問題となる可能性があります。

```js
const $input = document.createElement('input');
// この `click` イベントは今後記録されるようになります
$input.addEventListener('click', event => console.log(event));
// ここで `<input>` はまだ `document` に追加されていません
$input.click();
```
