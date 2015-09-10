---
title: "`HTMLInputElement.inputmode` has been disabled by default"
date: "2013-02-06T08:44:10-05:00"
categories: ["dom"]
tags: []
versions: "21"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=857355": "Bug 857355 – Hide HTMLInputElement\'s inputMode API behind a pref and only turn it on for Aurora/Nightly"
---
[`HTMLInputElement`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLInputElement)'s `inputmode` API, which has been [implemented](https://bugzilla.mozilla.org/show_bug.cgi?id=746142) since Firefox 17, is now disabled by default because the spec is still unstable. You have to enable the `dom.forms.inputmode` pref or use the [Aurora](http://www.mozilla.org/en-US/firefox/aurora/) channel to try out this feature. Note that this API will be [renamed `inputMode` (capitalized `M`) in Firefox 22](https://www.fxsitecompat.com/en-US/docs/2013/htmlmediaelement-crossorigin-and-htmlinputelement-inputmode-have-been-renamed/).
