---
title: "Several `appearance` keywords have been removed"
date: "2019-06-15T19:33:00-04:00"
categories: ["css"]
tags: []
releases: ["69"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1554150"
      title: "Bug 1554150 - Remove -webkit-appearance keywords that are removed in Chromium 75"
---
As of Firefox 69, several keywords for the `-webkit-appearance` CSS property and its alias `-moz-appearance` are no longer available from web content, following the removal in Chrome 75. These keywords include:

* `button-bevel`
* `caret`
* `listitem`
* `menulist-text`
* `menulist-textfield`
