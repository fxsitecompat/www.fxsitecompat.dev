---
title: "Behaviour of `-moz-user-select:none` has been changed to be consistent with `-moz-user-select:-moz-none` and other browsers"
date: "2013-02-06T08:44:10-05:00"
categories: ["css"]
tags: []
versions: ["21"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=816298"
      title: "Bug 816298 – Change \"-moz-user-select:none\" to behave like WebKit, IE, and Opera (and \"-moz-user-select:-moz-none\")"
aliases:
    - "/docs/2013/behavior-of-moz-user-select-none-has-been-changed-to-be-consistent-with-moz-user-select-moz-none-and-other-browsers/"
---
Previously, when you set the [`none`](https://developer.mozilla.org/en-US/docs/Web/CSS/none) keyword to the [`user-select`](https://developer.mozilla.org/en-US/docs/Web/CSS/user-select) property, the text of on the element and sub-elements became unselectable, even if one of those sub-elements had `-moz-user-select:text`. Starting with Firefox 21, `none` behaves like `-moz-none` and other browsers, so selection can be re-enabled on sub-elements using `-moz-user-select:text`.
