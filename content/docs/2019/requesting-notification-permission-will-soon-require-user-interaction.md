---
title: "Requesting notification permission will soon require user interaction"
date: "2019-11-01T23:07:00-04:00"
categories: ["dom"]
tags: []
versions: ["72"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1592959"
      title: "Bug 1592959 - Warn about non-user interaction Notification requests"
    - url: "https://blog.nightly.mozilla.org/2019/04/01/reducing-notification-permission-prompt-spam-in-firefox/"
      title: "Reducing Notification Permission Prompt Spam in Firefox – Firefox Nightly News"
---
Firefox currently allows to request push notification permission with no user interaction in the browser, but that kind of practice will stop working in the near future in an effort to prevent prompt spam. The Nightly and early Beta/DevEdition channels have already enabled the user interaction requirement since Firefox 68. Firefox 72 and later will show a deprecation warning in the web console for such cases. The [`Notification.requestPermission`](https://developer.mozilla.org/docs/Web/API/Notification/requestPermission) method must always be called from inside a short running user-generated event handler, such as `click` or `keydown`.
