---
title: "`Permissions.query`'s `userVisible` option has been renamed to `userVisibleOnly`"
date: "2016-04-24T06:34:00-04:00"
categories: ["dom"]
tags: []
versions: ["48"]
statuses: "affected"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1261405"
      title: "Bug 1261405 - PushPermissionDescriptor in Permissions.webidl is wrong ('userVisible' should be 'userVisibleOnly')"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1250902"
      title: "Bug 1250902 - Push notifications from http://simple-push-demo.appspot.com/ stopped working"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1266821"
      title: "Bug 1266821 - Remove PushPermissionDescriptor from the Permissions API"
---
The `userVisible` option for the [`Permissions.query`](https://developer.mozilla.org/en-US/docs/Web/API/Permissions/query) and [`revoke`](https://developer.mozilla.org/en-US/docs/Web/API/Permissions/revoke) methods, implemented with Firefox 46 and 47 respectively, has been renamed to `userVisibleOnly` as per the latest Push API spec.

Firefox actually throws a `NS_ERROR_NOT_IMPLEMENTED` exception when `userVisibleOnly` is set to `true`, because Firefox relies on its own quota system instead of this option, unlike Google Chrome. One demo app is broken with this change. There's a plan to remove the support for `PushPermissionDescriptor` itself from Firefox so that the option will just be ignored rather than throwing.
