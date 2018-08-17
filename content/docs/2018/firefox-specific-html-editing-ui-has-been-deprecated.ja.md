---
title: "Firefox 固有の HTML 編集 UI が廃止予定となりました"
date: "2018-08-17T13:28:00-04:00"
categories: ["html"]
tags: []
versions: ["63"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1449564"
      title: "Bug 1449564 - Disable table/image resizers in default"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/6GDK3Kzu9q0/discussion"
      title: "Intent to disable (hide) Gecko specific editing UI of HTML editor by default"
---
以下に挙げる [HTML リッチテキストエディター](https://developer.mozilla.org/docs/Web/Guide/HTML/Editable_content) 上の編集 UI 機能は、今のところ Firefox にしか実装されていませんが、廃止予定となったため、Firefox 63 の時点で Firefox Nightly と早期 Beta/DevEdition では初期設定により無効化されました。特に大きな問題がなければ、これらの機能は Firefox 64 ですべてのチャンネルから削除されます。

1. `<img>`、`<table>`、絶対配置要素のオブジェクトサイズ変更
2. インラインテーブル編集による列や行の追加・削除
3. 絶対配置要素の位置変更ハンドル

今のところ、1 と 2 は [`document.execCommand`](https://developer.mozilla.org/docs/Web/API/Document/execCommand) メソッドの `enableObjectResizing`、`enableInlineTableEditing` コマンドで無効化できます。3 を無効化する方法はありません。
