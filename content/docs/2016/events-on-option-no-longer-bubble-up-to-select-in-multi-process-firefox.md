---
title: "Events on `<option>` no longer bubble up to `<select>` in multi-process Firefox"
date: "2016-02-16T09:23:00-05:00"
categories: ["dom"]
tags: []
versions: ["43"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1090602"
      title: "Bug 1090602 - [e10s] <option> events do not bubble up through parent <select>"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/9Li1-qBaM88/discussion"
      title: "mozilla.dev.platform: Proposal to converge with Chromium / Blink for not firing events on <option>’s from <select> dropdowns"
---
On Firefox, [keyboard events](https://developer.mozilla.org/docs/Web/API/KeyboardEvent) and [mouse events](https://developer.mozilla.org/docs/Web/API/MouseEvent) fired on an [`<option>`](https://developer.mozilla.org/docs/Web/HTML/Element/option) element are bubbling up through the parent [`<select>`](https://developer.mozilla.org/docs/Web/HTML/Element/select) element, while such bubbling doesn't occur on Google Chrome. This behaviour actually [varies by browsers](https://bugzilla.mozilla.org/show_bug.cgi?id=1090602#c27) because the detail is not defined in the HTML spec yet.

For a better Web compatibility and technical reasons, those events will not bubble up when the `<select>` element is displayed as a dropdown list and [Firefox is running in the multi-process mode](https://www.fxsitecompat.dev/en-CA/docs/2015/multi-process-is-enabled-by-default-on-the-developer-edition/). The behaviour remains the same if `<select>` is displayed inline where it has the `multiple` attribute or the `size` attribute with a value greater than `1`.
