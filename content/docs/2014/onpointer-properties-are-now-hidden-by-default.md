---
title: "`onpointer*` properties are now hidden by default"
date: "2014-09-01T22:12:15-04:00"
categories: ["dom"]
tags: []
releases: ["34", "38-esr"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1017086"
      title: "Bug 1017086 – Don\'t expose onpointer* on global when dom.w3c_pointer_events.enabled is false"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1015600"
      title: "Bug 1015600 – Mobile Google Play menu does not work on Firefox for Android (pointerdown and pointerup events do not fire even though feature detection indicates support)"
---
Previously, pointer event handlers, including `onpointerup`, `onpointerover`, `onpointerout`, `onpointermove`, `onpointerleave`, `onpointerenter`, `onpointerdown` and `onpointercancel`, were accidentally exposed on the global object even when the [Pointer Events API](https://www.w3.org/TR/pointerevents/) was disabled. The API has not yet been enabled by default. This bug was affecting *Google Play* where a feature detection using `onpointerup` was working but the event itself was never fired. These properties are no longer exposed when the API is disabled.
