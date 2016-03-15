---
title: "一部の `KeyboardEvent.key` の値が廃止予定となりました"
date: "2014-07-22T05:06:26-04:00"
categories: ["dom"]
tags: []
versions: ["33"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1024864"
      title: "Bug 1024864 – For renaming some key values of KeyboardEvent.key on 33, we should warn it on the Console"
---
[`KeyboardEvent.key`](https://developer.mozilla.org/ja/docs/Web/API/KeyboardEvent.key) のいくつかの値が廃止予定となり、Firefox 34 での最新 DOM3 仕様に準拠した変更に先立ち [Web コンソール](https://developer.mozilla.org/ja/docs/Tools/Web_Console) に警告が表示されるようになりました。これには、`Down`、`Left`、`Right`、`Up`、`Crsel`、`Del`、`Exsel`、`Menu`、`Esc`、`Nonconvert`、`HalfWidth`、`RomanCharacters`、`FullWidth`、`SelectMedia`、`MediaNextTrack`、`MediaPreviousTrack`、`Red`、`Green`、`Yellow`、`Blue`、`Live`、`Apps`、`FastFwd`、`Zoom`、`DeadKeys` が含まれます。キー値の完全な一覧は [`KeyboardEvent.key`](https://developer.mozilla.org/ja/docs/Web/API/KeyboardEvent.key) ドキュメントを参照してください。

**更新**: 廃止予定となっていたこれらのキー値 [Firefox 37 で削除されました](https://www.fxsitecompat.com/ja/docs/2015/keyboardevent-key-values-have-been-updated-for-the-latest-spec/)。
