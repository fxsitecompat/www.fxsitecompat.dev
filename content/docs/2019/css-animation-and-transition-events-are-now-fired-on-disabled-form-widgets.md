---
title: "CSS animation and transition events are now fired on disabled form widgets"
date: "2019-05-12T21:29:00-04:00"
categories: ["css", "dom"]
tags: []
releases: ["67", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1530239"
      title: "Bug 1530239 - css transition events must fire even if an element is disabled"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1531605"
      title: "Bug 1531605 - css animation events must fire even if an element is disabled"
---
Starting with Firefox 67, CSS animation and transition events, including `animationend` and `transitionend`, will be fired on a form element like `<input>`, `<textarea>`, `<button>` and `<select>` even when it's disabled.

Just like a similar change in [Firefox 65](https://www.fxsitecompat.dev/en-CA/docs/2018/events-are-now-dispatched-on-disabled-form-widgets/) that allowed to fire mouse events on such a element, you might want to check the `disabled` property in your event handler to avoid any unexpected behaviour.
