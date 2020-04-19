---
title: "`location.hash` がシングルクォートをエスケープしなくなりました"
date: "2017-09-21T02:20:00-04:00"
categories: ["dom"]
tags: []
versions: ["57", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1386683"
      title: "Bug 1386683 - Firefox escapes single quote when accessing window.location properties via javascript"
---
Firefox は従来、[`Location`](https://developer.mozilla.org/docs/Web/API/Location)、[`URL`](https://developer.mozilla.org/docs/Web/API/URL) その他類似インターフェイス上の [`hash`](https://developer.mozilla.org/docs/Web/API/HTMLHyperlinkElementUtils/hash) プロパティでページの URL フラグメントに含まれるシングルクォートを取得する際、それらをエスケープしていました。このため、例えば `#foo'bar` の代わりに `#foo%27bar` が得られる状態でした。

これは関連仕様や他のブラウザーの挙動と一致していなかったことから、エスケープしないよう Firefox 57 で実装が修正されました。この変更は、コード内で Firefox 向けの特別な処理を行っていた場合に影響を及ぼす可能性があります。
