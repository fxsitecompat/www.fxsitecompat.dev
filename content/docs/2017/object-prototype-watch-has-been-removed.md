---
title: "`Object.prototype.watch()` has been removed"
date: "2017-10-24T16:27:00-04:00"
categories: ["javascript"]
tags: []
versions: ["58"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=638054"
      title: "Bug 638054 - JavaScript Object.prototype.watch should be removed, once an adequate debugger-only replacement exists"
---
The non-standard [`Object.prototype.watch`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object/watch) and [`unwatch`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object/unwatch) methods, deprecated since [Firefox 57](https://www.fxsitecompat.com/en-CA/docs/2017/object-prototype-watch-has-been-deprecated/), have been removed with Firefox 58. Use the standard [`Proxy`] (https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Proxy) or [`Reflect`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Reflect) object instead.

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
