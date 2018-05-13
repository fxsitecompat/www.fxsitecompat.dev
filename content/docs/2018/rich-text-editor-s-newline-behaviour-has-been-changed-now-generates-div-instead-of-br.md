---
title: "Rich text editor's newline behaviour has been changed, now generates `<div>` instead of `<br>`"
date: "2018-02-16T10:30:00-05:00"
categories: ["dom", "html"]
tags: []
versions: ["60"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1297414"
      title: "Bug 1297414 - Generate <p>/<div> for newlines, not <br> (defaultParagraphSeparator)"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1430551"
      title: "Bug 1430551 - Make defaultPargraphSeparater <div> in release build"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/V7LMopGp5HY/discussion"
      title: "Intent to change editor newline behavior"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/X2bhfUG49RE/discussion"
      title: "Intent to enable <div> as default paragraph separator of contenteditable/designMode editor by default"
aliases:
    - "/en-CA/docs/2017/rich-text-editor-s-newline-behaviour-has-been-changed-now-generates-div-instead-of-br/"
---
In Firefox, hitting the Enter key on a [rich text editor](https://developer.mozilla.org/docs/Rich-Text_Editing_in_Mozilla) inserts a `<br>` element, while Internet Explorer generates `<p>` and Google Chrome adds `<div>`. After much discussion, Firefox 60 changes the behaviour to match Chrome, so `<div>` will be used as the new default separator.

If you type "Firefox" and hit Enter between "Fire" and "fox", the result HTML would be `<div>Fire</div><div>fox</div>` instead of `Fire<br>fox`.

This behaviour, already enabled by default on Firefox Nightly and early Beta/DevEdition since version 55, can be controlled using the [`DefaultParagraphSeparator`](https://msdn.microsoft.com/en-us/library/hh801229(v=vs.85).aspx#DefaultParagraphSeparator) command for the [`execCommand`](https://developer.mozilla.org/docs/Web/API/Document/execCommand) method.

```js
// To insert <br> as before
document.execCommand("DefaultParagraphSeparator", false, "br");
// To generate <p> instead
document.execCommand("DefaultParagraphSeparator", false, "p");
```
