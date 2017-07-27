---
title: "`Permissions.revoke()` has been disabled"
date: "2016-08-17T13:50:00-04:00"
categories: ["dom"]
tags: []
versions: ["51"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1295877"
      title: "Bug 1295877 - Put Permissions API .revoke() behind a pref"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/x6XgGCoXUw0/discussion"
      title: "Intent to put Permission API's .revoke() method behind a pref"
---
The [`Permissions.revoke`](https://developer.mozilla.org/en-US/docs/Web/API/Permissions/revoke) method on the [Permissions API](https://developer.mozilla.org/en-US/docs/Web/API/Permissions_API) is now disabled by default because it has been shipped prematurely with Firefox 47 while the spec is not stable yet at this moment. It will eventually be re-enabled or removed depending on the progress of the standardization work.
