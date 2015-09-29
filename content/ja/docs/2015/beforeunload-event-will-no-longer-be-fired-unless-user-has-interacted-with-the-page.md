---
title: "`beforeunload` イベントはユーザがページ上で操作をしない限り発動されなくなりました"
date: "2015-09-29T10:25:00-04:00"
categories: ["dom"]
tags: []
versions: "44"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=636905": "Bug 636905 - Don't allow onbeforeunload dialog unless I have interacted with the page"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=578828": "Bug 578828 - Default to not allowing onbeforeunload dialogs"
---
[`beforeunload`](https://developer.mozilla.org/ja/docs/Web/Events/beforeunload) イベントは、特に隠し [`<iframe>`](https://developer.mozilla.org/ja/docs/Web/HTML/Element/iframe) を使って、ポップアップウィンドウを表示させる目的で乱用されることがしばしばあります。Firefox は、ポップアップブロック機能を強化するため、ユーザがページ上でクリック、タッチ、スクロール、文字入力といった何らかのインタラクションを起こさない限り、`beforeunload` イベントハンドラを無視するようになりました。

また、すべての `beforeunload` イベントハンドラを初期設定で不許可とする計画もあるため、Web 開発者にはこの種類のイベントの使用を避けるよう推奨します。Web ページやアプリは、[Web Storage API](https://developer.mozilla.org/ja/docs/Web/API/Web_Storage_API) や [IndexedDB API](https://developer.mozilla.org/ja/docs/Web/API/IndexedDB_API) でローカルに、あるいは [Ajax](https://developer.mozilla.org/ja/docs/Ajax) テクニックを使ってリモートにドラフト状態を保存することで、データ消失を防ぎつつユーザ体験を向上させることが可能です。
