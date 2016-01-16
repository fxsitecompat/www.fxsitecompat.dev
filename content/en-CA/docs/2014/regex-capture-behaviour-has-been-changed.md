---
title: "Regex capture behaviour has been changed"
date: "2014-09-01T22:12:15-04:00"
categories: ["javascript"]
tags: []
versions: ["34"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=369778": "Bug 369778 – Javascript regular expression captures broken with alternation in some cases."
aliases:
    - "/docs/2014/regex-capture-behavior-has-been-changed/"
---
In regular expressions, including `String.replace`, the matched text for a capturing group will be `undefined` instead of an empty string when the quantifiers prevented the group from being consulted (see also [this sample code](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp#Gecko-specific_notes)). Note that, for backward compatibility, `RegExp.$N` will still return an empty string rather than `undefined` ([bug 1053944](https://bugzilla.mozilla.org/show_bug.cgi?id=1053944)).

A performance regression of regular expressions introduced with Firefox 32 has also been fixed with Firefox 34. This issue might have lead to an "unresponsive script" dialog on Firefox 32 and 33 when using [`String.match`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/match), for example.
