---
title: "Flash Player can no longer always be activated"
date: "2019-06-15T23:03:00-04:00"
categories: ["plugins"]
tags: []
versions: ["69"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1519434"
      title: "Bug 1519434 - Remove \"Always Activate\" and \"Remember this decision\" Flash options in Firefox 69"
---
As part of the ongoing [Flash plug-in support deprecation](https://www.fxsitecompat.dev/en-CA/docs/2018/flash-plug-in-support-will-be-removed-in-2020/), Firefox 69 has removed the "Always Activate" option from the page notification dialog and the "Remember this decision" option from the Add-on Manager. It means, from now on, Firefox will ask the user every time if they want to show Flash content on a website during a browser session, and the user won't be able to change this behaviour.

At the time of this writing, only half of Firefox users have Flash Player installed according to [Firefox Public Data Report](https://data.firefox.com/dashboard/hardware), and the number is steadily decreasing. Given that the Flash support will be removed from Firefox and other browsers in 2020, you are strongly encouraged to make a migration plan as soon as possible if your site still relies on any Flash content including legacy video players.
