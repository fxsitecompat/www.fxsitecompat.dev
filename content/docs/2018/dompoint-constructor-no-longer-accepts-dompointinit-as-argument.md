---
title: "`DOMPoint` constructor no longer accepts `DOMPointInit` as argument"
date: "2018-05-23T22:20:00-04:00"
categories: ["css", "dom"]
tags: []
versions: ["62"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1186265"
      title: "Bug 1186265 - Remove DOMPoint{,ReadOnly}(DOMPointInit) constructor, implement DOMPoint{,ReadOnly}.fromPoint"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/jwmkVmU4DNM/discussion"
      title: "Intent to ship: DOMPoint interface from its latest spec"
---
Firefox 62 has updated the implementation of the [`DOMPoint`](https://developer.mozilla.org/docs/Web/API/DOMPoint) and [`DOMPointReadOnly`](https://developer.mozilla.org/docs/Web/API/DOMPointReadOnly) interfaces to the current Geometry Interfaces Module draft spec.

These [constructors](https://developer.mozilla.org/docs/Web/API/DOMPoint/DOMPoint) will no longer take a `DOMPointInit` dictionary containing an `x` coordinate, a `y` coordinate, a `z` coordinate and a `w` perspective, which have to be specified by separate arguments for the constructor. Alternatively, You can use the new `DOMPoint.fromPoint` and `DOMPointReadOnly.fromPoint` static methods that accept a `DOMPointInit` dictionary as the argument.

```js
// Don't do this
let dp = new DOMPoint({ x, y, z, w });

// Do this
let dp = new DOMPoint(x, y, z, w);
// or
let dp = DOMPoint.fromPoint({ x, y, z, w });
```
