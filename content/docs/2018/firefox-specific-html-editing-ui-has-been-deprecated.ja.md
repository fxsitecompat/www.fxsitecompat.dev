---
title: "Firefox 固有の HTML 編集 UI が廃止予定となりました"
date: "2018-08-17T13:28:00-04:00"
categories: ["html"]
tags: []
releases: ["63", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1449564"
      title: "Bug 1449564 - Disable table/image resizers in default"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/6GDK3Kzu9q0/discussion"
      title: "Intent to disable (hide) Gecko specific editing UI of HTML editor by default"
---
以下に挙げる [HTML リッチテキストエディター](https://developer.mozilla.org/docs/Web/Guide/HTML/Editable_content) 上の編集 UI 機能は、今のところ Firefox にしか実装されていませんが、廃止予定となったため、Firefox 63 の時点で Firefox Nightly と早期 Beta/DevEdition では初期設定により無効化されました。特に大きな問題がなければ、これらの機能は Firefox 64 ですべてのチャンネルにおいて初期設定により無効化されます。

* `<img>`、`<table>`、絶対配置要素のオブジェクトサイズ変更
* インラインテーブル編集による列や行の追加・削除
* 絶対配置要素の位置変更ハンドル

ウェブ開発者は今後も以下のように [`document.execCommand`](https://developer.mozilla.org/docs/Web/API/Document/execCommand) メソッドを使ってこれらの機能を有効化できますが、この UI は他のブラウザーでは利用できず、将来的には Firefox からも削除される可能性があることに留意してください。

```js
document.execCommand('enableObjectResizing', false, true);
document.execCommand('enableInlineTableEditing', false, true);
document.execCommand('enableAbsolutePositionEditor', false, true);
```

**更新**: この記事の初回草稿は、これらの機能が Firefox 64 で削除されるという記述をしていました。しかし、現在の計画では次回リリースで初期設定により無効化されるだけです。記事の内容はそれを受けて修正されました。

**更新 2**: [Firefox 64](https://www.fxsitecompat.dev/ja/docs/2018/firefox-specific-html-editing-ui-has-been-disabled-by-default/) 以降、予定通りこれらの機能はすべての Firefox チャンネルにおいて初期設定で無効化されています。
