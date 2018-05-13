---
title: "`Number` がバイナリーと 8 進数リテラルに対応しました"
date: "2014-12-19T11:15:21-05:00"
categories: ["javascript"]
tags: []
versions: ["36"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1079120"
      title: "Bug 1079120 – Make ToNumber(string) support binary and octal literals"
---
[`Number`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number) オブジェクトが、新しい ECMAScript 6 草案の通りにバイナリーリテラルと 8 進数リテラルに対応しました。このため、従来いずれも [`NaN`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/NaN) を返していた `Number('0b11')` と `Number('0o77')` が、それぞれ `3` と `63` を返すようになります。
