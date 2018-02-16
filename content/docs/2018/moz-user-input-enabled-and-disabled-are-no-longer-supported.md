---
title: "`-moz-user-input:enabled` and `disabled` are no longer supported"
date: "2018-02-16T10:39:00-05:00"
categories: ["css"]
tags: []
versions: ["60"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1405087"
      title: "Bug 1405087 - JavaScript: The \"click ()\" event isn`t executing from the script after deleting/setting to \"false\" the \"disabled\" prop of the element \"input type = submit\""
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/E6tfP__wkwg/discussion"
      title: "Intent to unship: -moz-user-input: disabled / enabled"
---
Firefox 60 has removed the support for the `enabled` and `disabled` values of the non-standard [`-moz-user-input`](https://developer.mozilla.org/en-US/docs/Web/CSS/-moz-user-input) CSS property because the usage is very low, and those were actually broken when changed dynamically. While `none` and the default `auto` value are still supported, the property itself may also be entirely removed in the future. Given that no other browsers support this property, the compatibility risk should be low.
