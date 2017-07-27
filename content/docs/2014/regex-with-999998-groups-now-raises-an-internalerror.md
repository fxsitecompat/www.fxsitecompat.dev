---
title: "Regex with 999998+ groups now raises an `InternalError`"
date: "2014-02-07T11:57:09-05:00"
categories: ["javascript"]
tags: []
versions: ["29"]
statuses: "regressed"
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=953013"
      title: "Bug 953013 – Regexp groups can overflow some counter"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=998785"
      title: "Bug 998785 – an error occurred while executing regular expression"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=976446"
      title: "Bug 976446 – Replace YARR with irregexp"
---
Starting with Firefox 29, [regular expressions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions) with more than 999998 groups will not work, rather raise an `InternalError` say "an error occurred while executing regular expression". This change aims to improve both performance and security by preventing the counters from being overflowed. See [Egor Homakov's blog post](http://homakov.blogspot.ca/2013/12/regexp-groups-overflow-in-ff.html) for details.

Regressions from this change have been reported that some specific regular expressions wrongly cause an `InternalError` where the regex previously claimed "no match" even if they should be matched. It has been discovered that the `trim` function in older versions of jQuery is also affected. This issue has been fixed with Firefox 30.
