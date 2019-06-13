---
title: "Non-standard `flags` argument has been removed from `String` search methods"
date: "2016-05-10T10:34:00-04:00"
categories: ["javascript"]
tags: []
versions: ["49"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1108382"
      title: "Bug 1108382 - Remove non-standard flag argument from String.prototype.{search,match,replace}"
aliases:
    - "/en-CA/docs/2015/non-standard-flags-argument-will-be-removed-from-string-search-methods/"
---
The non-standard `flags` argument of the [`String.prototype.search`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/search), [`match`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/match) and [`replace`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/replace) methods, [deprecated since Firefox 39](https://www.fxsitecompat.dev/en-CA/docs/2015/non-standard-flags-argument-of-string-methods-has-been-deprecated/) and [disabled in non-release builds since Firefox 47](https://www.fxsitecompat.dev/en-CA/docs/2016/non-standard-flags-argument-of-string-methods-has-been-disabled-in-non-release-builds/), is now completely removed.
