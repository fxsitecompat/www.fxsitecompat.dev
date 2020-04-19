---
title: "Image with `id` no longer appears on `document` unless it has `name` as well"
date: "2016-03-10T12:15:00-05:00"
categories: ["dom"]
tags: []
versions: ["45", "45-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1223523"
      title: "Bug 1223523 - Named getter on document should not return images with empty name"
---
Previously, images with an `id` attribute were always available on [`document`](https://developer.mozilla.org/docs/Web/API/Document), so that `<img id="foo">` was accessible via `document.foo`. This behaviour has been changed to comply with the spec, and now images with an `id` attribute as well as a non-empty `name` attribute will only create named properties on `document`. For a better cross-browser compatibility, it is recommended to always use the [`document.getElementById`](https://developer.mozilla.org/docs/Web/API/Document/getElementById) method instead.
