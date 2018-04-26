---
title: "`navigator.doNotTrack` now returns a correct value"
date: "2014-06-09T02:46:54-04:00"
categories: ["dom"]
tags: []
versions: ["32"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=887703"
      title: "Bug 887703 – Do not track settings results in wrong value for navigator.doNotTrack"
---
Previously, the [`navigator.doNotTrack`](https://developer.mozilla.org/en-US/docs/Web/API/navigator.doNotTrack) property was incorrectly returning `"yes"` even when the [Do Not Track](https://www.mozilla.org/dnt/) option was being disabled by the user. Starting with Firefox 32, it returns `"0"` (disabled), `"1"` (enabled) or `"unspecified"` to follow the spec.
