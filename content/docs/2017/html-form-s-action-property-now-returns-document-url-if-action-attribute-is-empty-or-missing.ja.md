---
title: "HTML フォームの `action` 属性が空か未設定の場合、`action` プロパティがドキュメント URL を返すようになりました"
date: "2017-11-10T00:54:00-05:00"
categories: ["dom", "html"]
tags: []
versions: ["56"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1366361"
      title: "Bug 1366361 - Make form.action return the actual form submission URL"
---
Firefox 56 以降、`<form>` HTML 要素上の `action` 属性が空になっているか設定されていない場合、それに対応する [`HTMLFormElement`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLFormElement) DOM オブジェクトの `action` プロパティは、空文字列の代わりに実際のフォーム送信先 URL、つまりドキュメントの URL を返します。

`<button>` や `<input>` 要素上の `formaction` 属性を反映した [`HTMLButtonElement`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLButtonElement) や [`HTMLInputElement`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLInputElement) オブジェクト上の `formAction` プロパティにも同じことが当てはまります。

この変更は最新の HTML 仕様に準拠するため行われ、今のところ 1 件のみ互換性問題が報告されています。他のブラウザーはまだ仕様に従っていないことから、こうした問題は本稿執筆時点では Firefox 上でのみ発生する可能性があります。

以下のように、ウェブ開発者が新旧両方の挙動に対応するのは簡単です。

```js
// これまで通り空文字列を得る (後方互換性)
let action_url = form.action === document.URL ? "" : form.action;

// 実際の送信先 URL を得る (前方互換性)
let actual_action_url = form.action || document.URL;
```
