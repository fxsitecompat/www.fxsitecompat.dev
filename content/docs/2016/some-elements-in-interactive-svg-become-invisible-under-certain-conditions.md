---
title: "Some elements in interactive SVG become invisible under certain conditions"
date: "2016-03-24T17:36:00-04:00"
categories: ["svg"]
tags: []
versions: ["45"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1258650"
      title: "Bug 1258650 - Yahoo finance chart comparison \"overlays\" not displayed properly because of bad interaction with scaled clip and mask combo"
---
Firefox 45 has introduced a regression where some elements within a complicated and interactive SVG may become invisible under certain circumstances, requiring unnecessary user interactions to show those elements. This bug is affecting stock charts on *Yahoo! Finance*. Mozilla developers will be working on the solution.

**Update**: This bug has been fixed with Firefox 46 Beta.
