---
title: "Intl API now uses browser locale by default on all platforms"
date: "2017-06-20T01:37:00-04:00"
categories: ["javascript"]
tags: []
versions: ["55"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1346674"
      title: "Bug 1346674 - Migrate all uses of nsILocaleService::GetApplicationLocale to mozILocaleService::GetAppLocale"
---
Firefox for macOS, Linux and Android were previously using the operating system's locale setting for the ECMAScript Internationalization API if no locale is specified by the programmer. Firefox 55 and later will rather use the browser locale as the default value on not only Windows but all platforms.

The affected object and methods include:

* [`Intl.DateTimeFormat`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/DateTimeFormat)
* [`Date.prototype.toLocaleString`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Date/toLocaleString)
* [`Date.prototype.toLocaleDateString`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Date/toLocaleDateString)

This may lead to a date format change for some Firefox users. For example, the browser locale is `en-US` while the platform uses `en-CA`, the return value of the `toLocaleDateString` method would be `6/20/2017` instead of `2017-06-20`.

Web developers may want to specify the optional `locales` argument for the API, probably using the current page's locale, to achieve consistent results.
