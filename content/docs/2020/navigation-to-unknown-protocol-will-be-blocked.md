---
title: "Navigation to unknown protocol will be blocked"
date: "2020-04-07T02:02:00-04:00"
categories: ["dom"]
tags: []
releases: ["76"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1528305"
      title: "Bug 1528305 - Behavior on meta and location.href redirects to an unknown protocol can break pages."
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/AaXUQ_t51D4/discussion"
      title: "Intent to implement and ship: Ignore navigation to unknown protocol"
---
Previously, Firefox was showing an error page saying “The address wasn’t understood” when a web page attempted to navigate to an unknown protocol using `location.href`, `<meta http-equiv="refresh">` or similar method. This behaviour had caused an user experience issue on various sites that tried to open their own external application.

Starting with Firefox 76, such page navigations/redirects will be ignored like Google Chrome, and Web Console will log a warning: “Prevented navigation to ... due to an unknown protocol.”

If you need to launch an external application or simply check if an external application is installed, you can instead use either `window.open()` or an `<iframe>`.
