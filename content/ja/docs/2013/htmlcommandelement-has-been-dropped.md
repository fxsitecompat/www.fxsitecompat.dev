---
title: "`HTMLCommandElement` が削除されました"
date: "2013-05-19T07:35:00-04:00"
categories: ["dom"]
tags: []
versions: ["24"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=857116"
      title: "Bug 857116 – Remove nsIDOMHTMLCommandElement"
---
廃止された `HTMLCommandElement` インターフェイスの実装が削除され、標準化された [`HTMLMenuItemElement`](https://developer.mozilla.org/ja/docs/Web/API/HTMLMenuItemElement) インターフェイスに置き換えられました。なお、Firefox は従来から [`<command>`](https://developer.mozilla.org/ja/docs/Web/HTML/Element/command) 要素には対応していません。
