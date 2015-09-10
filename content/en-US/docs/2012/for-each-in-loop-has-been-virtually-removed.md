---
title: "`for each...in` loop has been virtually removed"
date: "2012-12-29T08:29:30-05:00"
categories: ["javascript"]
tags: []
versions: "20"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=804834": "Bug 804834 – Hide \"for each\" from content"
---
While [E4X](https://developer.mozilla.org/en-US/docs/E4X) has been [deprecated and disabled since Firefox 17](https://www.fxsitecompat.com/en-US/docs/2012/e4x-has-been-disabled/), the [`for each...in`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for_each...in) statement, standardized as a part of that, has been left for backward compatibility. In Firefox 20, a change has been made to disable the statement unless Web developers explicitly specify JavaScript 1.6 and later like `<script type="text/javascript;version=1.6">`. You are recommended to replace with the [`for...of`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for...of) statement that are standardizing in [ECMAScript 6](https://developer.mozilla.org/en-US/docs/Web/JavaScript/ECMAScript_6_support_in_Mozilla).
