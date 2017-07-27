---
title: "Non-standard `flags` argument of `String` methods has been disabled in non-release builds"
date: "2016-02-08T05:13:00-05:00"
categories: ["javascript"]
tags: []
versions: ["47"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1245801"
      title: "Bug 1245801 - Disable non-standard flag argument of String.prototype.{search,match,replace} in non-release build."
---
The non-standard `flags` argument of the [`String.prototype.search`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/search), [`match`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/match) and [`replace`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/replace) methods, [deprecated since Firefox 39](https://www.fxsitecompat.com/en-CA/docs/2015/non-standard-flags-argument-of-string-methods-has-been-deprecated/), is now disabled in Firefox Nightly and Developer Edition. Do not use the argument anymore; it will be completely [removed in the near future](https://www.fxsitecompat.com/en-CA/docs/2015/non-standard-flags-argument-will-be-removed-from-string-search-methods/).

**Update**: The `flags` argument has been removed completely with Firefox 49.
