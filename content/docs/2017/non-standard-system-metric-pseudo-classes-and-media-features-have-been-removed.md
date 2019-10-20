---
title: "Non-standard system metric pseudo-classes and media features have been removed"
date: "2017-10-06T10:12:00-04:00"
categories: ["css"]
tags: []
versions: ["58"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1396066"
      title: "Bug 1396066 - Avoid exposing :-moz-system-metric stuff in content pages."
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1035774"
      title: "Bug 1035774 - Implement Interaction Media Features including pointer:coarse that replaces non-standard -moz-touch-enabled"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1406631"
      title: "Bug 1406631 - Remove color-picker-available system metric."
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1408838"
      title: "Bug 1408838 - Remove physical-home-button media feature."
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1408839"
      title: "Bug 1408839 - Hide some moz-scrollbar media features in content docs."
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/RVttfrQkXLU/discussion"
      title: "Intent to unship: :-moz-system-metric pseudo-class and media queries in content pages."
---
The non-standard, `moz`-prefixed system metric pseudo-classes and media features are no longer available from web content because those CSS extensions could be abused for fingerprinting purposes.

The pseudo-classes starting with `:-moz-system-metric`, such as [`:-moz-system-metric(mac-graphite-theme)`](https://developer.mozilla.org/docs/Web/CSS/:-moz-system-metric(mac-graphite-theme)), [`:-moz-system-metric(scrollbar-end-backward)`](https://developer.mozilla.org/docs/Web/CSS/:-moz-system-metric(scrollbar-end-backward)) and [`:-moz-system-metric(touch-enabled)`](https://developer.mozilla.org/docs/Web/CSS/:-moz-system-metric(touch-enabled)), have been removed.

The following media features have also been removed:

* `-moz-color-picker-available`
* `-moz-is-glyph`
* [`-moz-mac-graphite-theme`](https://developer.mozilla.org/docs/Web/CSS/@media/-moz-mac-graphite-theme)
* `-moz-mac-yosemite-theme`
* [`-moz-os-version`](https://developer.mozilla.org/docs/Web/CSS/@media/-moz-os-version)
* `-moz-overlay-scrollbars`
* `-moz-physical-home-button`
* [`-moz-scrollbar-end-backward`](https://developer.mozilla.org/docs/Web/CSS/@media/-moz-scrollbar-end-backward)
* [`-moz-scrollbar-end-forward`](https://developer.mozilla.org/docs/Web/CSS/@media/-moz-scrollbar-end-forward)
* [`-moz-scrollbar-start-backward`](https://developer.mozilla.org/docs/Web/CSS/@media/-moz-scrollbar-start-backward)
* [`-moz-scrollbar-start-forward`](https://developer.mozilla.org/docs/Web/CSS/@media/-moz-scrollbar-start-forward)
* [`-moz-scrollbar-thumb-proportional`](https://developer.mozilla.org/docs/Web/CSS/@media/-moz-scrollbar-thumb-proportional)
* `-moz-swipe-animation-enabled`
* [`-moz-windows-accent-color-in-titlebar`](https://developer.mozilla.org/docs/Web/CSS/@media/-moz-windows-accent-color-in-titlebar)
* [`-moz-windows-classic`](https://developer.mozilla.org/docs/Web/CSS/@media/-moz-windows-classic)
* [`-moz-windows-compositor`](https://developer.mozilla.org/docs/Web/CSS/@media/-moz-windows-compositor)
* [`-moz-windows-default-theme`](https://developer.mozilla.org/docs/Web/CSS/@media/-moz-windows-default-theme)
* [`-moz-windows-glass`](https://developer.mozilla.org/docs/Web/CSS/@media/-moz-windows-glass)
* [`-moz-windows-theme`](https://developer.mozilla.org/docs/Web/CSS/@media/-moz-windows-theme)

The only exception is the [`-moz-touch-enabled`](https://developer.mozilla.org/docs/Web/CSS/@media/-moz-touch-enabled) media feature which will be kept until the standard alternative [Interaction Media Features](https://drafts.csswg.org/mediaqueries-4/#mf-interaction) are implemented in Firefox.

**Update**: `-moz-touch-enabled` has been deprecated since [Firefox 71](https://www.fxsitecompat.dev/en-CA/docs/2019/moz-touch-enabled-media-feature-has-been-deprecated/).
