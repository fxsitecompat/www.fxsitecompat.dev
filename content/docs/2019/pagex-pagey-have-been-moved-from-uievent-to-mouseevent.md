---
title: "`pageX`/`pageY` have been moved from `UIEvent` to `MouseEvent`"
date: "2019-07-06T22:22:00-04:00"
categories: ["dom"]
tags: []
versions: ["69"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1178763"
      title: "Bug 1178763 - TouchEvent.pageX/pageY should be undefined"
---
The `pageX` and `pageY` properties, previously available on the `UIEvent` interface, have been moved to the `MouseEvent` interface, because the implementation of Firefox didn't comply with the spec. It means these properties are no longer exposed to the `CompositionEvent`, `FocusEvent`, `InputEvent`, `KeyboardEvent` and `TouchEvent` interfaces which all inherit from `UIEvent`.

[Google Chrome](https://groups.google.com/a/chromium.org/d/topic/blink-dev/pcMwyHRhbCU/discussion) has already made the same change in version 45, and this bug fix should improve web interoperability.
