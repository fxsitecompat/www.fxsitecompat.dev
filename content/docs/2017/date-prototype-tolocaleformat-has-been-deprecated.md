---
title: "`Date.prototype.toLocaleFormat` has been deprecated"
date: "2017-08-01T20:07:00-04:00"
categories: ["javascript"]
tags: []
versions: ["55"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1299900"
      title: "Bug 1299900 - Warn when Date.prototype.toLocaleFormat is used"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1344625"
      title: "Bug 1344625 - Turn on ENABLE_INTL_API=yes on Android's release build"
---
The support for the non-standard [`Date.prototype.toLocaleFormat`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Date/toLocaleFormat) method is now considered deprecated and will be [removed](https://www.fxsitecompat.com/en-CA/docs/2015/date-prototype-tolocaleformat-will-be-removed/) in the near future. Firefox 55 and later shows a warning in the Console for the method.

There are JavaScript libraries like [Sugar](https://sugarjs.com/) to achieve the same results. You can also use the standard [`toLocaleDateString`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Date/toLocaleDateString) method, which is a part of the [ECMAScript Internationalization API](https://hacks.mozilla.org/2014/12/introducing-the-javascript-internationalization-api/), as the following examples illustrate:

```js
// Formats like "Tuesday, August 1, 2017"
(new Date()).toLocaleFormat('%A, %B %e, %Y');
// can be replaced with
(new Date()).toLocaleString('en-US', {
  year: 'numeric',
  month: 'long',
  day: 'numeric',
  weekday: 'long',
});
```

```js
// Formats like "2017-08-01 20:07:13"
(new Date()).toLocaleFormat('%Y-%m-%d %H:%M:%S');
// can be replaced with
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

Note that the Intl API is available on Firefox 56 and later on Android, while the desktop version of Firefox has already added the support with Firefox 29.

**Update**: This method has been removed with [Firefox 58](https://www.fxsitecompat.com/en-CA/docs/2017/date-prototype-tolocaleformat-has-been-removed/).
