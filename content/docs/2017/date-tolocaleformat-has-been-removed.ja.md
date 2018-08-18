---
title: "`Date.toLocaleFormat()` が削除されました"
date: "2017-10-25T17:27:00-04:00"
categories: ["javascript"]
tags: []
versions: ["58"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=818634"
      title: "Bug 818634 - Remove support for Date.prototype.toLocaleFormat"
aliases:
    - "/ja/docs/2015/date-prototype-tolocaleformat-will-be-removed/"
    - "/ja/docs/2017/date-prototype-tolocaleformat-has-been-removed/"
---
[Firefox 55](https://www.fxsitecompat.com/ja/docs/2017/date-prototype-tolocaleformat-has-been-deprecated/) 以降廃止予定となっていた [`Date.prototype.toLocaleFormat`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Date/toLocaleFormat) メソッドは、標準化されなかったため、Firefox 58 で削除されました。Firefox 以外どのブラウザーもこのメソッドを実装していません。

例えば [Sugar](https://sugarjs.com/) のように同じ結果を得られる JavaScript ライブラリがあります。また、以下の例が示すように、[ECMAScript Internationalization API](https://hacks.mozilla.org/2014/12/introducing-the-javascript-internationalization-api/) の一部である標準の [`toLocaleDateString`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Date/toLocaleDateString) メソッドを使用することもできます。

```js
// "Tuesday, August 1, 2017" のような形式
(new Date()).toLocaleFormat('%A, %B %e, %Y');
// これは以下のように置き換えられます
(new Date()).toLocaleString('en-US', {
  year: 'numeric',
  month: 'long',
  day: 'numeric',
  weekday: 'long',
});
```

```js
// "2017-08-01 20:07:13" のような形式
(new Date()).toLocaleFormat('%Y-%m-%d %H:%M:%S');
// これは以下のように置き換えられます
(new Date()).toLocaleString('en-US', {
  year: 'numeric',
  month: '2-digit',
  day: '2-digit',
  hour: '2-digit',
  minute: '2-digit',
  second: '2-digit',
  hour12: false,
}).replace(/(\d+)\/(\d+)\/(\d+),\s(.*)/, '$3-$1-$2 $4');
```
