---
title: "`navigator.battery` has been deprecated in favour of async `getBattery` method"
date: "2015-09-13T23:41:00-04:00"
categories: ["dom"]
tags: []
versions: ["43"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1047119": "Bug 1047119 - Update Battery Status API to match latest Editors draft: navigator.getBattery(), etc"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1050749": "Bug 1050749 - Expose BatteryManager via getBattery() returning a Promise instead of a synchronous accessor (navigator.battery)."
aliases:
    - "/docs/2015/navigator-battery-has-been-deprecated-in-favor-of-async-getbattery-method/"
---
The [Battery Status API](https://developer.mozilla.org/en-US/docs/Web/API/Battery_Status_API) implementation has been updated to match the [latest spec](http://www.w3.org/TR/battery-status/). The [`navigator.battery`](https://developer.mozilla.org/en-US/docs/Web/API/Navigator/battery) property is now deprecated in favour of the standardized [`navigator.getBattery`](https://developer.mozilla.org/en-US/docs/Web/API/Navigator/getBattery) method that returns a [`Promise`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise) for the [`BatteryManager`](https://developer.mozilla.org/en-US/docs/Web/API/BatteryManager) interface. The `battery` property support will be removed in the future.
