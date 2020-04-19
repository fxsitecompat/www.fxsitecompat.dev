---
title: "`window.localStorage` がプライバシー設定によってブロックされた場合に `SecurityError` を投げなくなりました"
date: "2019-05-13T02:15:00-04:00"
categories: ["dom", "privacy-security"]
tags: []
versions: ["67", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1529396"
      title: "Bug 1529396 - Consider relaxing the exception-throwing semantics of window.localStorage when a privacy check fails"
---
`window.localStorage` は従来、ユーザーのプライバシー設定によって使用できない場合、具体的には Cookie が無効となっている際に `SecurityError` 例外を投げていました。Firefox 67 以降、このプロパティはそうした場合単に `null` となり、JavaScript に適切な `try-catch` 処理が書かれていないため一部のサイトが読み込まれない問題を解消します。

```js
// なお、window.localStorage が null となる場合、
// これは引き続き TypeError を投げます
window.localStorage.setItem(key, value);

// そのため以下のように書く必要があります。
const storage = window.localStorage;

if (storage) {
  // ストレージを使用
  storage.setItem(key, value);
}
```

**更新**: この変更は互換性に関する懸念から Firefox 70 で取り消されました。`window.localStorage` は再度 `SecurityError` を投げるようになります。
