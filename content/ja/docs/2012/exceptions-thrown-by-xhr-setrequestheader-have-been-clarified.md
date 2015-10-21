---
title: "`XHR.setRequestHeader()` で投げられる例外が明確化されました"
date: "2012-12-03T03:50:54-05:00"
categories: ["dom"]
tags: []
versions: ["17"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=600111": "Bug 600111 – XMLHttpRequest.setRequestHeader() throws NS_ERROR_FAILURE inappropriately"
---
`XMLHttpRequest` の [`setRequestHeader`](https://developer.mozilla.org/ja/docs/DOM/XMLHttpRequest#setRequestHeader%28%29) 関数で投げられる例外コードは、従来どんなエラーであっても `NS_ERROR_FAILURE` となっていました。エラーを適切に区別できるよう、仕様で定義された 2 種類の例外コード、`NS_ERROR_DOM_INVALID_STATE_ERR` と `NS_ERROR_DOM_SYNTAX_ERR` が使われるようになりました。
