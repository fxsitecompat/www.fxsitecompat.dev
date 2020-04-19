---
title: "`Date.parse()` no longer accepts illegal ISO 8601 date/time formats"
date: "2019-06-10T00:44:00-04:00"
categories: ["javascript"]
tags: []
versions: ["68", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1500748"
      title: "Bug 1500748 - Date.parse accepts illegal non-zero-padded ISO8601 format"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1550949"
      title: "Bug 1550949 - Disallow time-only version of ISO8601"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1551893"
      title: "Bug 1551893 - Disallow non-zero-padded time element in Date.parse if time part marker T exists"
---
It has been found that the `Date.parse` static method in Firefox was successfully parsing some illegal ISO 8601 date/time formats. The implementation has been corrected with Firefox 68, and these values will result in `NaN` from now on:

* `2018-1-7T00:00Z` (no padded zeros in the date, should be `2018-01-07T00:00Z`)
* `2019-05-15T1:1:1` (no padded zeros in the time, should be `2019-05-15T01:01:01`)
* `T00:00:00Z` (no date)
