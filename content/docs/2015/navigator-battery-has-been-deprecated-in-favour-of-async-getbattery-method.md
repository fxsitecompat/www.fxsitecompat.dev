---
title: "`navigator.battery` has been deprecated in favour of async `getBattery` method"
date: "2015-09-13T23:41:00-04:00"
categories: ["dom"]
tags: []
versions: ["43"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1047119"
      title: "Bug 1047119 - Update Battery Status API to match latest Editors draft: navigator.getBattery(), etc"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1050749"
      title: "Bug 1050749 - Expose BatteryManager via getBattery() returning a Promise instead of a synchronous accessor (navigator.battery)."
aliases:
    - "/en-CA/docs/2015/navigator-battery-has-been-deprecated-in-favor-of-async-getbattery-method/"
---
The [Battery Status API](https://developer.mozilla.org/docs/Web/API/Battery_Status_API) implementation has been updated to match the [latest spec](https://www.w3.org/TR/battery-status/). The [`navigator.battery`](https://developer.mozilla.org/docs/Web/API/Navigator/battery) property is now deprecated in favour of the standardized [`navigator.getBattery`](https://developer.mozilla.org/docs/Web/API/Navigator/getBattery) method that returns a `Promise` resolved in a [`BatteryManager`](https://developer.mozilla.org/docs/Web/API/BatteryManager) instance. The `battery` property support will be removed in the future.

**Update**: `navigator.battery` has been [removed with Firefox 50](https://www.fxsitecompat.com/en-CA/docs/2016/navigator-battery-has-been-removed-in-favour-of-async-getbattery-method/).

**Update**: The Battery Status API has been [removed with Firefox 52](https://www.fxsitecompat.com/en-CA/docs/2016/battery-status-api-has-been-removed/).
