---
title: "Checkboxes and radio buttons are not displayed when `MSThemeCompatible` is `no`"
date: "2017-06-17T01:45:00-04:00"
categories: ["html"]
tags: []
versions: ["54"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=169373"
      title: "Bug 169373 - Use nsITheme with HTML form controls"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=605985"
      title: "Bug 605985 - -moz-appearance:none should make checkboxes and radios be non-replaced elements (except on Android)"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=966240"
      title: "Bug 966240 - Drop support for MSThemeCompatible"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1373417"
      title: "Bug 1373417 - Checkboxes and radio buttons are not displayed on Firefox 54+ when <meta http-equiv=\"MSTHEMECOMPATIBLE\" content=\"no\"> is specified"
aliases:
    - "/docs/2017/checkboxes-and-radio-buttons-are-not-displayed-when-msthemecompatible-is-disabled/"
---
Firefox 54 has changed the way HTML checkboxes and radio buttons are rendered, so `<input type="radio">` and `<input type="checkbox">` are no longer [replaced elements](https://developer.mozilla.org/en-US/docs/Web/CSS/Replaced_element) when styled with `-moz-appearance:none`. It will give web developers more flexibility in designing form controls.


This change, however, has produced an unexpected side effect where those types of elements become invisible if `<meta http-equiv="MSThemeCompatible" content="no">` exists in the document `<head>`.

According to an [MSDN article](https://msdn.microsoft.com/en-us/library/ms533876(v=vs.85).aspx), the `<meta>` tag in question "disables theme support for the document" on Internet Explorer for Windows XP, and Firefox has also maintained the partial compatibility for a long time. Meanwhile, no other browsers, including Google Chrome and Microsoft Edge, support the non-standard, obscure feature.

This rendering regression has been solved with Firefox 55 by dropping the support for `MSThemeCompatible`. Web developers can work around the issue by simply removing the obsolete `<meta>` tag from the site.
