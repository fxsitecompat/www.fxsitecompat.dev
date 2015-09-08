---
title: "Indexed properties on the `window` object (ie. `iframe`s) are now enumerable"
date: "2013-02-06T08:44:10-05:00"
categories: ["dom"]
tags: []
versions: "21"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=823228": "Bug 823228 - Move indexed properties from nsWindowSH::GetProperty to the outer window proxy"
---
Previously, [`<iframe>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/iframe) in the DOM were not enumerable on the [`window`](https://developer.mozilla.org/en-US/docs/Web/API/window) object. This behavior has been changed to comply with the spec, which means they are now returned with `Object.keys(window)`. This is important to note for things like global leak detection, since appending `iframe`s to the document will modify the enumerable keys on the `window` object.
