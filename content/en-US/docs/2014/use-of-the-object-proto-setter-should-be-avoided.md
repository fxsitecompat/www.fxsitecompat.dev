---
title: "Use of the `Object.__proto__` setter should be avoided"
date: "2014-03-21T04:50:04-04:00"
categories: ["javascript"]
tags: []
versions: "30"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=948227": "Bug 948227 – Make the Object.prototype.__proto__ setter warn about perf impact when used, and suggest alternatives"
---
Mutating the prototype of an object, using either [`Object.__proto__`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/proto) or [`Object.setPrototypeOf`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/setPrototypeOf), is strongly discouraged because the operation is very slow. While Internet Explorer 11 added the support of `Object.__proto__` for interoperability, this property has been deprecated and should not be used. Firefox 30 and later warns the usage of the `Object.__proto__` setter when the JavaScript strict warning is enabled. As described in the documents, the [`Object.create`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/create) method should be used instead to create an object with a desired prototype.
