---
title: "`Date.toLocaleFormat()` が廃止予定となりました"
date: "2017-08-01T20:07:00-04:00"
categories: ["javascript"]
tags: []
versions: ["55", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1299900"
      title: "Bug 1299900 - Warn when Date.prototype.toLocaleFormat is used"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1344625"
      title: "Bug 1344625 - Turn on ENABLE_INTL_API=yes on Android's release build"
aliases:
    - "/ja/docs/2017/date-prototype-tolocaleformat-has-been-deprecated/"
---
非標準 [`Date.prototype.toLocaleFormat`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Date/toLocaleFormat) メソッドへの対応が廃止予定となり、近い将来 [削除される](https://www.fxsitecompat.dev/ja/docs/2015/date-prototype-tolocaleformat-will-be-removed/) こととなりました。Firefox 55 以降、コンソールにこのメソッドに対する警告が表示されます。

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

なお、Intl API は Android では Firefox 56 以降で使用可能となっています。一方デスクトップ版 Firefox では Firefox 29 で既に対応が追加されています。

**更新**: このメソッドは [Firefox 58](https://www.fxsitecompat.dev/ja/docs/2017/date-prototype-tolocaleformat-has-been-removed/) で削除されました。
