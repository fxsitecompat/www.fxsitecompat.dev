---
title: "Generator now returns `IteratorResult` instead of throwing"
date: "2014-02-07T11:57:09-05:00"
categories: ["javascript"]
tags: []
versions: ["29"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=958951"
      title: "Bug 958951 – Return IteratorResult object for completed generators instead of throwing"
---
The ECMAScript 6 compliant syntax for [Generators (yield)](http://wiki.ecmascript.org/doku.php?id=harmony:generators) has been introduced with [Firefox 26](https://developer.mozilla.org/Firefox/Releases/26). The implementation has been updated for the latest spec, and a completed generator function now returns an `IteratorResult` object like `{ value: undefined, done: true }` instead of throwing a [`TypeError`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/TypeError). This behaviour matches the iterator of the [`Array`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array), [`Map`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Map) and [`Set`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Set) interfaces, that the implementation has been [updated with Firefox 27](https://www.fxsitecompat.dev/en-CA/docs/2013/iterator-implementation-has-been-updated-to-the-latest-spec/).
