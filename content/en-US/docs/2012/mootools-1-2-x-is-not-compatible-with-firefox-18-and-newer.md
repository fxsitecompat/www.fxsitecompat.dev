---
title: "Mootools 1.2.x is not compatible with Firefox 18 and newer"
date: "2012-12-03T03:53:26-05:00"
categories: ["javascript"]
tags: []
versions: "18"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=789036": "Bug 789036 – Mootools 1.2.x was broken by String.prototype.contains"
---
Firefox 18 adds the ECMAScript 6 function [`String.prototype.contains`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/contains). Unfortunately, old version of Mootools assume there is no such function, and fail to work when it exists. This problem is fixed in Mootools 1.3 and newer.
