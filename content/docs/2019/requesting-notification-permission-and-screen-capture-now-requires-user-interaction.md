---
title: "Requesting notification permission and screen capture now requires user interaction"
date: "2019-11-11T20:16:00-05:00"
categories: ["audio-video", "dom"]
tags: []
versions: ["72"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1524619"
      title: "Bug 1524619 - Require user gestures for push notifications"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1580944"
      title: "Bug 1580944 - Require user gesture for getDisplayMedia()"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1592959"
      title: "Bug 1592959 - Warn about non-user interaction Notification requests"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1593644"
      title: "Bug 1593644 - Enable dom.webnotifications.requireuserinteraction on Release"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/Mezd5pLjnJU/discussion"
      title: "Intent to Ship: Require user interaction for notification permission prompts"
    - url: "https://blog.mozilla.org/futurereleases/2019/11/04/restricting-notification-permission-prompts-in-firefox/"
      title: "Restricting Notification Permission Prompts in Firefox - Future Releases"
    - url: "https://hacks.mozilla.org/2019/11/upcoming-notification-permission-changes-in-firefox-72/"
      title: "Upcoming notification permission changes in Firefox 72 - Mozilla Hacks"
aliases:
    - "/en-CA/docs/2019/requesting-notification-permission-will-soon-require-user-interaction/"
    - "/en-CA/docs/2019/requesting-notification-permission-now-requires-user-interaction/"
---
Firefox had previously allowed to request push notification permission with no user interaction in the browser, but that kind of practice stopped working with Firefox 72 in an effort to prevent prompt spam. The Nightly and early Beta/DevEdition channels have already enabled the user interaction requirement since Firefox 68, and Firefox 71 shows a deprecation warning in the web console for such cases.

The [`Notification.requestPermission`](https://developer.mozilla.org/docs/Web/API/Notification/requestPermission) and [`PushManager.subscribe`](https://developer.mozilla.org/docs/Web/API/PushManager/subscribe) methods must always be called from inside a short running user-generated event handler, such as `click` or `keydown`.

The same policy applies to the [`MediaDevices.getDisplayMedia`](https://developer.mozilla.org/docs/Web/API/MediaDevices/getDisplayMedia) method that allows to capture the user's computer screen as an image (screenshot) or video (screencast).
