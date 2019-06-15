---
title: "`user-select` has been unprefixed"
date: "2019-06-15T19:33:00-04:00"
categories: ["css"]
tags: []
versions: ["69"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1492739"
      title: "Bug 1492739 - Consider unprefixing -moz-user-select"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/XfKl9Jt7ZQ8/discussion"
      title: "Intent to implement and ship: Unprefix -moz-user-select, unship mozilla-specific values."
---
The `user-select` CSS property has been unprefixed with Firefox 69 after the non-standard values were removed with [Firefox 65](https://www.fxsitecompat.dev/en-CA/docs/2018/non-standard-moz-user-select-values-have-been-removed/) except for `-moz-none`. The support for the prefixed `-moz-user-select` property may be removed in the future.
