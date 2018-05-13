---
title: "`Date.prototype.toLocaleFormat` has been removed"
date: "2017-10-25T17:27:00-04:00"
categories: ["javascript"]
tags: []
versions: ["58"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=818634"
      title: "Bug 818634 - Remove support for Date.prototype.toLocaleFormat"
aliases:
    - "/en-CA/docs/2015/date-prototype-tolocaleformat-will-be-removed/"
---
The support for the [`Date.prototype.toLocaleFormat`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Date/toLocaleFormat) method, deprecated since [Firefox 55](https://www.fxsitecompat.com/en-CA/docs/2017/date-prototype-tolocaleformat-has-been-deprecated/), has been removed with Firefox 58, because it failed to be standardized. No other browsers than Firefox implement the method.

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
