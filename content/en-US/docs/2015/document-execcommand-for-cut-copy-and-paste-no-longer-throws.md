---
title: "`document.execCommand` for cut, copy and paste no longer throws"
date: "2015-06-13T15:20:46-04:00"
categories: ["dom"]
tags: []
versions: "41"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1012662": "Bug 1012662 - Allow document.execCommand(\"cut\"/\"copy\") to be used within the context of user generated events"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1161721": "Bug 1161721 - Return false from document.queryCommandSupported(\"paste\") if calling execCommand(\"paste\") will fail"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1162952": "Bug 1162952 - Fix document.queryCommandEnabled(\'cut\'/\'copy\') to return true always"
---
Firefox now allows Web pages to modify the content of clipboard programmatically in user-generated event handlers, so click-to-copy actions, for instance, no longer require an alternative solution like Flash Player. See a [relevant thread](https://groups.google.com/d/topic/mozilla.dev.platform/oWhmLMvGAD0/discussion) on the dev-platform list and the [Mozilla Hacks blog](https://hacks.mozilla.org/2015/09/flash-free-clipboard-for-the-web/) for details.

This change has updated the implementation of [`document.execCommand`](https://developer.mozilla.org/en-US/docs/Web/API/Document/execCommand) and [`document.queryCommandEnabled`](https://developer.mozilla.org/en-US/docs/Web/API/Document/queryCommandEnabled), and those methods no longer throw for the `cut` and `copy` commands, instead return `true` in user-generated event handlers or `false` in other cases. The `paste` command still won't work for security reasons, and those methods will return `false`. The [`document.queryCommandSupported`](https://developer.mozilla.org/en-US/docs/Web/API/Document/queryCommandSupported) method now returns a correct value, instead of always returning `true`.
