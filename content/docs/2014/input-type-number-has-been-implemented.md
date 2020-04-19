---
title: "`<input type=\"number\">` has been implemented"
date: "2014-02-07T11:57:09-05:00"
categories: ["html"]
tags: []
releases: ["29", "31-esr"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=344616"
      title: "Bug 344616 – Implement <input type=\"number\">"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=946398"
      title: "Bug 950737 – Flip the pref to enable <input type=number>"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=947728"
      title: "Bug 947728 – Provide a way for content to hide <input type=number>\'s spinner"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1000400"
      title: "Bug 1000400 – skyscanner.com layout broken because site doesn\'t leave enough room for arrow buttons on <input type=\"number\">"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1008385"
      title: "Bug 1008385 – Betterment.com \"Goal set up\" page\'s funded-in-X-years input is broken, due to spinners pushing number out of view"
---
The [`<input>`](https://developer.mozilla.org/docs/Web/HTML/Element/input) element now supports the `number` type introduced with HTML5. At least 2 regressions from this change have been found, due to the addition of a spinner control. Page authors can hide the spinner using CSS [`-moz-appearance: textfield`](https://developer.mozilla.org/docs/Web/CSS/-moz-appearance) if needed. It's not part of any spec but works along with `-webkit-appearance: none` for Chrome.
