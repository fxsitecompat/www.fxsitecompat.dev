---
title: "Non-standard complex syntax is no longer supported in `-moz`-prefixed CSS gradients"
date: "2019-06-09T21:50:00-04:00"
categories: ["css"]
tags: []
versions: ["68", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1547939"
      title: "Bug 1547939 - Consider simplifying -moz-linear-gradient parsing"
---
While Firefox developers have decided not to drop the support for `-moz`-prefixed CSS gradients for backward compatibility, the parser has been simplified with Firefox 68 so the `-moz-linear-gradient`, `-moz-radial-gradient` and `-moz-repeating-linear-gradient` functions will be more like aliases of the standard equivalents.

The legacy complex syntax having both an angle and a position will no longer be parsed. These are some examples from the [patch](https://hg.mozilla.org/mozilla-central/rev/a484a2625d18):

```css
-moz-linear-gradient(20% bottom, red, blue);
-moz-radial-gradient(top left 45deg, red, blue);
-moz-repeating-linear-gradient(30grad left 35px, red, blue);
```

Meanwhile, for WebKit compatibility, a non-standard syntax without the `to` keyword like this will continue to be supported:

```css
-moz-linear-gradient(top, red, blue); /* has to be `to top` */
```

Web developers are still encouraged to use the unprefixed version of these CSS functions which are widely supported by now.
