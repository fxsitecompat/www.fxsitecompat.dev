---
title: "Most of non-standard CSS `display` values have been dropped"
date: "2018-06-02T20:25:00-04:00"
categories: ["css"]
tags: []
versions: ["62"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=879275"
      title: "Bug 879275 - Consider turning off -moz-box display types in untrusted stylesheets"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1288572"
      title: "Bug 1288572 - Hide -moz-prefixed display values from web content"
aliases:
    - "/en-CA/docs/2015/non-standard-css-display-types-will-be-removed/"
---
The non-standard, `-moz`-prefixed CSS [`display`](https://developer.mozilla.org/docs/Web/CSS/display) property values, originally intended for Mozilla application UI, are no longer available from web content. The standard [Flexible Box Layout](https://developer.mozilla.org/docs/Web/CSS/CSS_Flexible_Box_Layout) or [Grid Layout](https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout) should be used instead.

* `-moz-deck`
* `-moz-grid`
* `-moz-grid-group`
* `-moz-grid-line`
* `-moz-groupbox`
* `-moz-inline-grid`
* `-moz-inline-stack`
* `-moz-popup`
* `-moz-stack`

For the meantime, the following values will be left due to concerns over compatibility issues. Firefox developers are planning to use [Telemetry](https://wiki.mozilla.org/Telemetry) to understand the usage on the web before removing these exceptions.

* `-moz-box`
* `-moz-inline-box`
