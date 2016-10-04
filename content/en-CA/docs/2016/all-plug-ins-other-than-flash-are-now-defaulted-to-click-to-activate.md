---
title: "All plug-ins other than Flash are now defaulted to click-to-activate"
date: "2016-04-30T07:25:00-04:00"
categories: ["plugins"]
tags: []
versions: ["47"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1263630"
      title: "Bug 1263630 - Remove all plugins (except Flash) from the click-to-activate whitelist"
---
As part of the [NPAPI plug-in deprecation in Firefox](https://www.fxsitecompat.com/en-CA/docs/2015/plug-in-support-will-be-dropped-by-the-end-of-2016-except-flash/), all plug-ins except for Adobe Flash Player have been removed from the [plug-in whitelist introduced back in early 2014](https://www.fxsitecompat.com/en-CA/docs/2014/plugin-whitelist-has-been-implemented/). That means they will be reverted to the default click-to-activate behaviour on Firefox 47 and later. The NPAPI support except for Flash is planned to be removed with Firefox 53, therefore Web developers are strongly encouraged to use modern standard technologies instead.
