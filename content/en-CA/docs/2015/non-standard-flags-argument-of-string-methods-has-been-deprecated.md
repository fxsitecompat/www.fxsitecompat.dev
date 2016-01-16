---
title: "Non-standard `flags` argument of `String` methods has been deprecated"
date: "2015-03-17T14:02:59-04:00"
categories: ["javascript"]
tags: []
versions: ["39"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1142351": "Bug 1142351 - Add console warnings for non-standard flag argument of String.prototype.{search,match,replace}."
---
The non-standard `flags` argument of the [`String.prototype.search`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/search), [`match`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/match) and [`replace`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/replace) methods is now considered deprecated and will be removed in the near future. It raises a warning in the [Web Console](https://developer.mozilla.org/en-US/docs/Tools/Web_Console) from now on.
