---
title: "Browser UI can no longer be controlled with `window.open()` features parameter"
date: "2020-04-06T22:48:00-04:00"
categories: ["dom"]
tags: []
versions: ["76"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1507375"
      title: "Bug 1507375 - Can we drop window.open's feature parameter which controls UI parts visibility?"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/_3aWsRQ8Tfs/discussion"
      title: "Intent to ship: Restrict window.open features parameter"
---
Web developers can use the optional `windowFeatures` parameter for the [`window.open`](https://developer.mozilla.org/docs/Web/API/Window/open) method to define how a new tab or window should be displayed to the users, though the behaviour is [implementation-dependent](https://arai-a.github.io/window-open-features/).

Starting with Firefox 76, it will no longer be possible to control the browser’s user interface elements with certain window features such as `menubar`, `personalbar` and `toolbar`, which were only supported by Firefox and Internet Explorer. This change aims not only to align with other modern browsers but also to avoid unexpected behaviours due to UI customization or session restore.

These window features continue to be used as [conditions](https://hg.mozilla.org/mozilla-central/rev/bf0e49a9ceff#l9.12) for Firefox to decide whether to open a new tab or popup window.
