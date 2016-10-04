---
title: "Defining non-configurable property on `window` will throw (currently only on Nightly and Developer Edition)"
date: "2016-04-10T01:08:00-04:00"
categories: ["dom"]
tags: []
versions: ["42"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1107443"
      title: "Bug 1107443 - Make WindowProxy throw if you attempt to define a non-configurable property"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1178638"
      title: "Bug 1178638 - Turn on the exceptions from bug 1107443 (Object.defineProperty on window with non-configurable property) on beta/release"
aliases:
    - "/docs/2016/window-now-throws-when-defining-non-configurable-property-currently-only-on-nightly-and-developer-edition/"
---
Firefox 42 and later will throw a [`TypeError`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypeError) when you attempt to define a non-configurable property on [`window`](https://developer.mozilla.org/en-US/docs/Web/API/Window) with the [`Object.defineProperty`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/defineProperty) or [`Object.defineProperties`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/defineProperties) method. For now, this change has been made to Firefox Nightly and Developer Edition only. A couple of site compatibility issues have been found, and Mozilla developers are discussing the next step accordingly.
