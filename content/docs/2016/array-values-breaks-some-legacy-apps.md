---
title: "`Array.values()` breaks some legacy apps"
date: "2016-09-21T21:07:00-04:00"
categories: ["javascript"]
tags: []
versions: ["48"]
statuses: "reverted"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1299593"
      title: "Bug 1299593 - Microsoft Dynamics CRM 2011 Lookup Error since Firefox Version 48.0.2 due to Array.prototype.values"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1299444"
      title: "Bug 1299444 - Blank calendar section in MS Outlook webmail (OWA) after Firefox 48"
aliases:
    - "/en-CA/docs/2016/array-prototype-values-breaks-some-legacy-apps/"
---
Firefox 48 has added the support for the [`Array.prototype.values`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/values) method in ECMAScript 2015 (ES6). There are several reports of broken applications, including *Microsoft Dynamics CRM 2011* and *Outlook Web App*, due to the new method shipped with Microsoft Edge and Apple Safari as well. Mozilla developers are considering disabling it in Firefox.

**Update**: The `values` method has been disabled with Firefox 49.0.2 to avoid compatibility issues, though it's still available on Firefox Nightly.

**Update 2**: The method has been [re-enabled](https://www.fxsitecompat.dev/en-CA/docs/2018/array-prototype-values-is-now-enabled-again/) with Firefox 60.
