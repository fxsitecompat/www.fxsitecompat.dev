---
title: "`load` event is no longer fired on `<iframe>` with JavaScript `src` returning non-string value"
date: "2016-10-16T01:05:00-04:00"
categories: ["dom", "javascript"]
tags: []
versions: ["49"]
statuses: "reverted"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1268047"
      title: "Bug 1268047 - Change the handling of javascript: return values to align with other browsers and the updated spec"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1306472"
      title: "Bug 1306472 - No load event for iframe with javascript: URI that doesn't return a string"
---
On Firefox 49, the [`load`](https://developer.mozilla.org/docs/Web/Events/load) event is not fired on the `<iframe>` element when the source is JavaScript code that does not return a string, like this:

```html
<iframe src="javascript:true" onload="alert('hello')"></iframe>
```

This change was made to follow the latest HTML spec, however, there are several reports of broken sites after the release of Firefox 49. Firefox 49.0.2 has therefore reverted the backward incompatible change so that the event will be fired as before.
