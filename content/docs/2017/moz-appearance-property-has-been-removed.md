---
title: "`-moz-appearance` property has been removed"
date: "2017-02-15T15:00:00-05:00"
categories: ["css"]
tags: []
versions: ["future"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=605985"
      title: "Bug 605985 - -moz-appearance:none should make checkboxes and radios be non-replaced elements (except on Android)"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1333482"
      title: "Bug 1333482 - [css-ui] Implement 'appearance:auto | none', with '-webkit-appearance' as an alias."
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1351745"
      title: "Bug 1351745 - Disable -moz-appearance for non-UA/chrome sheets"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/oZ9cPF8Y1pE/discussion"
      title: "Intent to implement and ship CSS 'appearance' with '-webkit-appearance' as an alias. Unship '-moz-appearance'."
---
Firefox 54 has added the support for the CSS [`appearance`](https://developer.mozilla.org/docs/Web/CSS/appearance) property along with `-webkit-appearance` as an alias for WebKit/Blink compatibility. Meanwhile, the non-standard, Firefox-specific [`-moz-appearance`](https://developer.mozilla.org/docs/Web/CSS/-moz-appearance) property is no longer available to web content.

Both `appearance:none` and `-webkit-appearance:none` work in the same way as `-moz-appearance:none`, which turns off the native theme for elements. The initial value is `auto`.

**Update**: This change has been planned for Firefox 54 but postponed.
