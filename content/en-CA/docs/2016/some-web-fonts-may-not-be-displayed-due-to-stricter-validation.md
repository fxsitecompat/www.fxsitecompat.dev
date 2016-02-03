---
title: "Some Web fonts may not be displayed due to stricter validation"
date: "2016-02-03T13:19:00-05:00"
categories: ["misc"]
tags: []
versions: ["44"]
statuses: "affected"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1244693": "Bug 1244693 - FF 44 fails to load some WOFF fonts"
---
On Firefox 44 and later, some Web fonts may be rejected due to the stricter validation by a new version of the OpenType Sanitizer. Fonts containing OpenType layout tables that are violating the spec will not be rendered and the Web Console shows a warning about the error.

Due to a couple of affected sites including *Nokia*, Mozilla developers are considering loosening the validation on the Beta and Release channels. However, problematic fonts should be replaced anyway.
