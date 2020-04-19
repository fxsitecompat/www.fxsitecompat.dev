---
title: "Some Web fonts may not be displayed due to stricter validation"
date: "2016-02-03T13:19:00-05:00"
categories: ["misc"]
tags: []
versions: ["44", "45-esr"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1244693"
      title: "Bug 1244693 - FF 44 fails to load some WOFF fonts"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1331797"
      title: "Bug 1331797 - Can't load fonts on https://fonts.google.com/"
---
On Firefox 44 and later, some Web fonts may be rejected due to the stricter validation by a new version of the OpenType Sanitizer. Fonts containing OpenType layout tables that are violating the spec will not be rendered and the Web Console shows a warning about the error.

**Update**: Due to a couple of affected sites including *Nokia*, the validation has been loosened on the Beta and Release channels since Firefox 45. However, problematic fonts should be replaced anyway.

**Update 2**: Some fonts on [*Google Fonts*](https://fonts.google.com/) are also broken, showing "tofu" characters on Firefox Nightly and Developer Edition.

**Update 3**: The broken fonts on *Google Fonts* have been fixed by Google in October 2017.
