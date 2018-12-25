---
title: "`min`/`max-content` keywords for CSS sizing properties have been unprefixed"
date: "2018-12-25T00:32:00-05:00"
categories: ["css"]
tags: []
versions: ["66"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1322780"
      title: "Bug 1322780 - Unprefix min-content and max-content keywords"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/vyCAurCC2DI/discussion"
      title: "Intent to ship: unprefixed max-content and min-content for css sizing properties"
---
The `min-content` and `max-content` keywords that can be used for CSS sizing properties such as `width`, `height` and `flex-basis` are now available unprefixed in Firefox 66 and later. Google Chrome has supported the unprefixed keywords since the version 46.

The removal of the prefixed version, `-moz-min-content` and `-moz-max-content`, which will remain supported as the aliases, is yet to be announced.
