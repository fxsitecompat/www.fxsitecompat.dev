---
title: "`navigator.battery` has been removed in favour of async `getBattery` method"
date: "2016-06-07T10:08:00-04:00"
categories: ["dom"]
tags: []
versions: ["50"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1259335"
      title: "Bug 1259335 - Remove deprecated navigator.battery API"
---
The [`navigator.battery`](https://developer.mozilla.org/en-US/docs/Web/API/Navigator/battery) property, [deprecated since Firefox 43](https://www.fxsitecompat.com/en-CA/docs/2015/navigator-battery-has-been-deprecated-in-favour-of-async-getbattery-method/), has been removed with Firefox 50. Instead, use the standardized [`navigator.getBattery`](https://developer.mozilla.org/en-US/docs/Web/API/Navigator/getBattery) method that returns a `Promise` resolved in a [`BatteryManager`](https://developer.mozilla.org/en-US/docs/Web/API/BatteryManager) instance.

**Update**: The Battery Status API has been [removed with Firefox 52](https://www.fxsitecompat.com/en-CA/docs/2016/battery-status-api-has-been-removed/).
