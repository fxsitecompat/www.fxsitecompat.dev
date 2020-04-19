---
title: "`window.open()` can now be called only once per event"
date: "2018-12-21T00:52:00-05:00"
categories: ["dom"]
tags: []
releases: ["65", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=675574"
      title: "Bug 675574 - Do not allow more than one call to window.open() when we allow popups"
---
Firefox 65 has improved the pop-up blocker to prevent multiple pop-up windows from being opened at the same time. Calling the `window.open` method is now allowed only once per event, and any subsequent calls will be blocked by the browser. For a better user experience, opening multiple pop-ups or tabs should be avoided in any case.
