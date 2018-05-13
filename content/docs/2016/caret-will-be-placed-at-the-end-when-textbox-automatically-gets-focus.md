---
title: "Caret will be placed at the end when textbox automatically gets focus"
date: "2016-09-16T00:43:00-04:00"
categories: ["dom"]
tags: []
versions: ["51"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1287655"
      title: "Bug 1287655 - input/textarea selectionStart, selectionEnd should return cursor position when selection is empty"
---
Previously, when an `<input>` or `<textarea>` element received a focus with the [`focus`](https://developer.mozilla.org/docs/Web/API/HTMLElement/focus) method, a caret was initially placed at the beginning of the text, and therefore, both the `selectionStart` and `selectionEnd` properties on the form control would always be `0`.

Firefox 51 has changed the behaviour to follow the HTML spec, so that a caret will be placed at the end of the text, and these properties will be the same value as the text length. The [`setSelectionRange`](https://developer.mozilla.org/docs/Web/API/HTMLInputElement/setSelectionRange) method can be used to specify the selection range if needed.
