---
title: "HTML form's `action` property now returns document URL if `action` attribute is empty or missing"
date: "2017-11-10T00:54:00-05:00"
categories: ["dom", "html"]
tags: []
versions: ["56", "60-esr"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1366361"
      title: "Bug 1366361 - Make form.action return the actual form submission URL"
---
Starting with Firefox 56, if the `action` attribute on a `<form>` HTML element is empty or missing, the `action` property on the corresponding [`HTMLFormElement`](https://developer.mozilla.org/docs/Web/API/HTMLFormElement) DOM object will return the actual form submission URL, which is the document's URL, instead of an empty string.

The same applies to the `formAction` property on [`HTMLButtonElement`](https://developer.mozilla.org/docs/Web/API/HTMLButtonElement) and [`HTMLInputElement`](https://developer.mozilla.org/docs/Web/API/HTMLInputElement) objects that reflects the `formaction` attribute on the `<button>` or `<input>` element.

This change was made to be compliant the latest HTML spec, and so far only 1 compatibility issue has been reported. Since other browsers are not following the spec yet, such issues may only happen in Firefox at the time of this writing.

It's easy for Web developers to support both the old and new behaviour, like this:

```js
// To get an empty string as before (backward compatibility)
let action_url = form.action === document.URL ? "" : form.action;

// To get the actual submission URL (forward compatibility)
let actual_action_url = form.action || document.URL;
```
