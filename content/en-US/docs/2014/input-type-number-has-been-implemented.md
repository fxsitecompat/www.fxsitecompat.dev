---
title: "`<input type=\"number\">` has been implemented"
date: "2014-02-07T11:57:09-05:00"
categories: ["html"]
tags: []
versions: ["29"]
statuses: "affected"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=344616": "Bug 344616 – Implement <input type=\"number\">"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=946398": "Bug 950737 – Flip the pref to enable <input type=number>"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=947728": "Bug 947728 – Provide a way for content to hide <input type=number>\'s spinner"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1000400": "Bug 1000400 – skyscanner.com layout broken because site doesn\'t leave enough room for arrow buttons on <input type=\"number\">"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1008385": "Bug 1008385 – Betterment.com \"Goal set up\" page\'s funded-in-X-years input is broken, due to spinners pushing number out of view"
---
The [`<input>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input) element now supports the `number` type introduced with HTML5. At least 2 regressions from this change have been found, due to the addition of a spinner control. Page authors can hide the spinner using CSS [`-moz-appearance: textfield`](https://developer.mozilla.org/en-US/docs/Web/CSS/-moz-appearance) if needed. It's not part of any spec but works along with `-webkit-appearance: none` for Chrome.
