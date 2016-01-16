---
title: "2 `KeyboardEvent` location consts have been removed"
date: "2015-02-27T04:21:22-05:00"
categories: ["dom"]
tags: []
versions: ["38"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=936313": "Bug 936313 – Drop KeyboardEvent.DOM_LOCATION_MOBILE and KeyboardEvent.DOM_LOCATION_JOYSTICK of KeyboardEvent.location since they have been dropped from D3E spec"
---
The `DOM_LOCATION_MOBILE` and `DOM_LOCATION_JOYSTICK` constants have been removed from the [`KeyboardEvent`](https://developer.mozilla.org/en-US/docs/Web/API/KeyboardEvent) interface, since those have been dropped from the DOM3 Events spec.
