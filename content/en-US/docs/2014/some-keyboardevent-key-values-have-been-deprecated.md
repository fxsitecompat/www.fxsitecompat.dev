---
title: "Some `KeyboardEvent.key` values have been deprecated"
date: "2014-07-22T05:06:26-04:00"
categories: ["dom"]
tags: []
versions: "33"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1024864": "Bug 1024864 – For renaming some key values of KeyboardEvent.key on 33, we should warn it on the Console"
---
Some of [`KeyboardEvent.key`](https://developer.mozilla.org/en-US/docs/Web/API/KeyboardEvent.key) values are now considered deprecated and warned in the [Web Console](https://developer.mozilla.org/en-US/docs/Tools/Web_Console) prior to the change in Firefox 34 to comply with the latest DOM3 spec. Those include `Down`, `Left`, `Right`, `Up`, `Crsel`, `Del`, `Exsel`, `Menu`, `Esc`, `Nonconvert`, `HalfWidth`, `RomanCharacters`, `FullWidth`, `SelectMedia`, `MediaNextTrack`, `MediaPreviousTrack`, `Red`, `Green`, `Yellow`, `Blue`, `Live`, `Apps`, `FastFwd`, `Zoom` and `DeadKeys`. Check out the [`KeyboardEvent.key`](https://developer.mozilla.org/en-US/docs/Web/API/KeyboardEvent.key) document for the complete list of key values.
