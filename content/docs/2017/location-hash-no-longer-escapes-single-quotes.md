---
title: "`location.hash` no longer escapes single quotes"
date: "2017-09-21T02:20:00-04:00"
categories: ["dom"]
tags: []
versions: ["57"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1386683"
      title: "Bug 1386683 - Firefox escapes single quote when accessing window.location properties via javascript"
---
Previously, Firefox was escaping single quotes contained in the page's URL fragment when retrieving it with the [`hash`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLHyperlinkElementUtils/hash) property on the [`Location`](https://developer.mozilla.org/en-US/docs/Web/API/Location), [`URL`](https://developer.mozilla.org/en-US/docs/Web/API/URL) and similar interfaces, so you'd get `#foo%27bar` instead of `#foo'bar`, for example.

Since this didn't match the relevant specs and other browsers' behaviour, Firefox 57 has corrected the implementation not to escape single quotes. This change may break code if you have a special handling for Firefox.
