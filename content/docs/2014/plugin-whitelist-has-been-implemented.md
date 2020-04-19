---
title: "Plugin whitelist has been implemented"
date: "2014-03-21T04:50:04-04:00"
categories: ["plugins"]
tags: []
versions: ["30", "31-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=992995"
      title: "Bug 992995 – Implement plugin whitelist"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1007389"
      title: "Bug 1007389 – Implement plugin whitelist, round 2"
---
Mozilla has defined the [plugin whitelist policy](https://blog.mozilla.org/security/2014/02/28/update-on-plugin-activation/) since the Click-to-Activate functionality was [added to Firefox 26](https://www.fxsitecompat.dev/en-CA/docs/2013/java-is-now-defaulted-to-click-to-activate/). The whitelist has been implemented in Firefox 30 and plug-ins are now defaulted to click-to-activate except the registered ones. The complete list of whitelisted plug-ins is available in [this spreadsheet](https://docs.google.com/spreadsheets/d/19JIQiaS9mJgkKQ07ax2KH7syRCgxt2dCCxcBD56PiQc/edit?usp=sharing).
