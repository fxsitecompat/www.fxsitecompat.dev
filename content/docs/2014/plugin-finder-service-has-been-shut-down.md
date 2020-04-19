---
title: "Plugin Finder Service has been shut down"
date: "2014-10-17T22:50:44-04:00"
categories: ["plugins"]
tags: []
releases: ["35", "38-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=836415"
      title: "Bug 836415 – Kill PFS"
---
The [Plugin Finder Service](https://wiki.mozilla.org/PFS2), which allowed Firefox users to easily find a missing plugin with a "doorhanger" notification, has been discontinued as part of Mozilla's plugin support removal plan. Sites using a plugin content should provide visitors a link to the plugin vendor and eventually replace the content with a Web standards-based implementation.
