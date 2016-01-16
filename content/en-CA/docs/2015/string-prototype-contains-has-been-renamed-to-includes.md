---
title: "`String.prototype.contains` has been renamed to `includes`"
date: "2015-04-27T13:17:23-04:00"
categories: ["javascript"]
tags: []
versions: ["40"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1102219": "Bug 1102219 - Rename String.prototype.contains to String.prototype.includes"
---
The `String.prototype.contains` method, introduced with ECMAScript 6 and Firefox 18, had caused considerable site compatibility issues, notably with [*MooTools*](https://bugzilla.mozilla.org/show_bug.cgi?id=789036). The library has already fixed the issue, but in order to be consistent with [`Array.prototype.includes`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/includes), which has also renamed from `contains` due to compatibility issues, the specification has renamed the method to [`String.prototype.includes`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/includes). The Firefox implementation has been updated to match the spec. While the deprecated `contains` method still remains as an alias of `includes`, it will be [removed](https://www.fxsitecompat.com/en-CA/docs/2015/string-prototype-contains-will-be-removed/) in the near future.
