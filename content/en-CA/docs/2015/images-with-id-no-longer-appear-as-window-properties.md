---
title: "Images with `id` no longer appear as `window` properties"
date: "2015-10-21T00:53:00-07:00"
categories: ["dom"]
tags: []
versions: ["42"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=959992": "Bug 959992 - Firefox 26 creates enumerable properties on window for ids of <img> tags"
aliases:
    - "/docs/2015/imgs-with-id-no-longer-appear-as-window-properties/"
---
Starting with Firefox 26, [`<img>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/img) elements having the `id` attribute were appearing as enumerable properties on the [`window`](https://developer.mozilla.org/en-US/docs/Web/API/Window) object as per the HTML spec, so `<img id="logo">` for example was accessible via the `window.logo` property. The spec has later changed to switch back to the previous behaviour that matches Safari and Chrome. Firefox 42 has updated the implementation accordingly, therefore such images are no longer on `window`.
