---
title: "ES6 array methods have been added"
date: "2013-07-14T19:12:37-04:00"
categories: ["javascript"]
tags: []
versions: ["25", "31-esr"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=885553"
      title: "Bug 885553 – Implement ES6 Array.prototype.find and Array.prototype.findIndex"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=866849"
      title: "Bug 866849 – Implement ES6 Array.from and Array.of"
---
As part of [ECMAScript 6 support](https://developer.mozilla.org/docs/Web/JavaScript/ECMAScript_6_support_in_Mozilla), the [`Array.find`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/find), [`Array.findIndex`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/findIndex) and [`Array.of`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/of) methods have been added. [`Array.from`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/from) will also be added soon. This may break some JavaScript libraries which are extending [`Array.prototype`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/prototype) with their own methods. For now, at least one library, [*Sugar*](https://bugzilla.mozilla.org/show_bug.cgi?id=903755), is known to be affected. *Sugar* users should update to the latest version to avoid this conflict.
