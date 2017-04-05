---
title: "Rich text editor's newline behaviour has been changed, now generates `<div>` instead of `<br>`"
date: "2017-04-05T09:02:00-04:00"
categories: ["misc"]
tags: []
versions: ["55"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1297414"
      title: "Bug 1297414 - Generate <p>/<div> for newlines, not <br> (defaultParagraphSeparator)"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/V7LMopGp5HY/discussion"
      title: "Intent to change editor newline behavior"
---
In Firefox, hitting the Enter key on a [rich text editor](https://developer.mozilla.org/en-US/docs/Rich-Text_Editing_in_Mozilla) inserts a `<br>` element, while Internet Explorer generates `<p>` and Google Chrome adds `<div>`. After much discussion, Firefox 55 changes the behaviour to match Chrome, so `<div>` will be used as the new default separator.

If you type "Firefox" and hit Enter between "Fire" and "fox", the result HTML would be `<div>Fire</div><div>fox</div>` instead of `Fire<br>fox`.

This behaviour can be controlled using the [`DefaultParagraphSeparator`](https://msdn.microsoft.com/en-us/library/hh801229(v=vs.85).aspx#DefaultParagraphSeparator) command for the [`execCommand`](https://developer.mozilla.org/en-US/docs/Web/API/Document/execCommand) method.

```js
// To insert <br> as before
document.execCommand("DefaultParagraphSeparator", false, "br");
// To generate <p> instead
document.execCommand("DefaultParagraphSeparator", false, "p");
```
