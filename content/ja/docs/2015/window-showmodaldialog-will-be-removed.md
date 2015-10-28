---
title: "`window.showModalDialog` が削除されます"
date: "2015-10-27T22:25:00-07:00"
categories: ["dom"]
tags: []
versions: ["future"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=981796": "Bug 981796 - Remove window.showModalDialog"
---
[Firefox 28 以降廃止予定となっている](https://www.fxsitecompat.com/ja/docs/2013/showmodaldialog-has-been-deprecated/) [`window.showModalDialog`](https://developer.mozilla.org/ja/docs/Web/API/Window/showModalDialog) メソッドは、近い将来削除されます。標準の [`window.open`](https://developer.mozilla.org/ja/docs/Web/API/Window/open) メソッドか、独自のページ内モーダル UI を使ってください。HTML5 の [`<dialog>`](https://developer.mozilla.org/ja/docs/Web/HTML/Element/dialog) 要素がもうひとつの代替案となりますが、これはまだ Firefox には実装されていません。
