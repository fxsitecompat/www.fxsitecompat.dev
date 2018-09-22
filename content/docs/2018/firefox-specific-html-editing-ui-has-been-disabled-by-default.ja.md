---
title: "Firefox 固有の HTML 編集 UI が初期設定で無効化されました"
date: "2018-09-22T13:05:00-04:00"
categories: ["html"]
tags: []
versions: ["64"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1490641"
      title: "Bug 1490641 - Disable all Gecko specific UIs by default in release build"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/6GDK3Kzu9q0/discussion"
      title: "Intent to disable (hide) Gecko specific editing UI of HTML editor by default"
---
以下に挙げる [HTML リッチテキストエディター](https://developer.mozilla.org/docs/Web/Guide/HTML/Editable_content) 上の編集 UI 機能は、今のところ Firefox にしか実装されていませんが、W3C Editing Task Force の要請を受けて、Firefox 64 以降初期設定で無効化されました。これらは [廃止予定とされており](https://www.fxsitecompat.com/ja/docs/2018/firefox-specific-html-editing-ui-has-been-deprecated/)、既に Firefox 63 の時点で Firefox Nightly と早期 Beta/DevEdition では初期設定により無効化されています。

* `<img>`、`<table>`、絶対配置要素のオブジェクトサイズ変更
* インラインテーブル編集による列や行の追加・削除
* 絶対配置要素の位置変更ハンドル

ウェブ開発者は今後も以下のように [`document.execCommand`](https://developer.mozilla.org/docs/Web/API/Document/execCommand) メソッドを使ってこれらの機能を有効化できますが、この UI は他のブラウザーでは利用できず、将来的には Firefox からも削除される可能性があることに留意してください。

```js
document.execCommand('enableObjectResizing', false, true);
document.execCommand('enableInlineTableEditing', false, true);
document.execCommand('enableAbsolutePositionEditor', false, true);
```
