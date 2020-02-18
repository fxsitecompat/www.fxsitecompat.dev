---
title: "`click()` now works on elements outside of `document`"
date: "2020-02-17T23:48:00-05:00"
categories: ["dom"]
tags: []
versions: ["75"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1610821"
      title: "Bug 1610821 - Ensure click() works on input elements which are disconnected from a document"
---
Previously, Firefox had discarded the [`HTMLElement.click`](https://developer.mozilla.org/docs/Web/API/HTMLElement/click) method triggered on an element that wasn’t part of a `document`. On Firefox 74 and later, such method calls will work and the corresponding `click` event will be fired on that element. Since the new behaviour mostly aligns with other browsers, it’s unlikely to cause site compatibility issues. However, if a site is using a user-agent sniffing to run code specific to Firefox that assumes the `click` event will not be fired, this change could be a potential problem.

```js
const $input = document.createElement('input');
// This `click` event will be logged from now on
$input.addEventListener('click', event => console.log(event));
// Here the `<input>` is not yet added to the `document`
$input.click();
```
