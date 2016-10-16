---
title: "`load` event is no longer fired on `<iframe>` with JavaScript `src` returning non-string value"
date: "2016-10-16T01:05:00-04:00"
categories: ["dom", "javascript"]
tags: []
versions: ["49"]
statuses: "reverted"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1306472"
      title: "Bug 1306472 - No load event for iframe with javascript: URI that doesn't return a string"
---
On Firefox 49 and later, the `<iframe>` element will no longer fire a `load` event when the source is JavaScript code that does not return a string, like this:

```html
<iframe src="javascript:true" onload="alert('hello')"></iframe>
```

This change has been made to follow the latest HTML spec, however, there are several reports of broken sites after the release of Firefox 49. Firefox 49.0.2 has therefore restored the previous behaviour to avoid further compatibility issues.
