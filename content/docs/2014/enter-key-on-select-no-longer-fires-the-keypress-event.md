---
title: "Enter key on `<select>` no longer fires the `keypress` event"
date: "2014-02-07T11:57:09-05:00"
categories: ["dom"]
tags: []
releases: ["29"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=935876"
      title: "Bug 935876 – <select> element shouldn\'t consume key events which don\'t cause any default action"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1008244"
      title: "Bug 1008244 – Regression in 29: \"Enter\" key on <select> element no longer fires a keypress event"
---
The [`<select>`](https://developer.mozilla.org/docs/Web/HTML/Element/select) element without the `multiple` attribute no longer fires the [`keypress`](https://developer.mozilla.org/docs/Web/Reference/Events/keypress) event when the <kbd>Enter</kbd> key is pressed, to avoid an unintentional form submission. This issue has been fixed with Firefox 30. Developers can instead observe the [`keydown`](https://developer.mozilla.org/docs/Web/Reference/Events/keydown) event to do the same thing.
