---
title: "`Object.watch()` has been deprecated"
date: "2017-08-21T16:27:00-04:00"
categories: ["javascript"]
tags: []
versions: ["57", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=934669"
      title: "Bug 934669 - Deprecate Object.prototype.{,un}watch, and make them warn when used"
aliases:
    - "/en-CA/docs/2015/object-prototype-watch-will-be-removed/"
    - "/en-CA/docs/2017/object-prototype-watch-will-be-removed/"
    - "/en-CA/docs/2017/object-prototype-watch-has-been-deprecated/"
---
The non-standard [`Object.prototype.watch`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object/watch) and [`unwatch`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object/unwatch) methods are now considered deprecated and will be removed in the near future. Firefox 57 and later shows a warning in the Console for these methods that are not supported by any other browsers. Use the standard [`Proxy`] (https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Proxy) or [`Reflect`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Reflect) object instead.

The following example is a simple replacement of `Object.prototype.watch` by `Proxy`:

```js
const o = { a: 1 };

// Don't do this
o.watch('a', (prop, oldval, newval) => {
  console.log(`o.${prop} has been changed from ${oldval} to ${newval}`);
  return newval;
});

o.a = 2; // o.a has been changed from 1 to 2

// Do this
const p = new Proxy(o, {
  set: (obj, prop, newval) => {
    const oldval = obj[prop];
    obj[prop] = newval;
    console.log(`p.${prop} has been changed from ${oldval} to ${newval}`);
    return true;
  }
});

p.a = 3; // p.a has been changed from 2 to 3
```

**Update**: These methods have been removed with [Firefox 58](https://www.fxsitecompat.dev/en-CA/docs/2017/object-prototype-watch-has-been-removed/).
