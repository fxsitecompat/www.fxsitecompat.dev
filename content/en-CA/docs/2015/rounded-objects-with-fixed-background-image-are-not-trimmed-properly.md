---
title: "Rounded objects with fixed background image are not trimmed properly"
date: "2015-12-18T17:37:00-05:00"
categories: ["css"]
tags: []
versions: ["43"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1232939"
      title: "Bug 1232939 - The background image in a div is causing a spill over of the border where the border-radius cuts into the div"
---
Firefox 43 has introduced a regression where a combination of the `background-image` and `border-radius` CSS properties is not drawn as expected if the `background-attachment` is `fixed`, leaving monochromatic, angulated corners around the object. Mozilla developers are working on the solution.

**Update**: This bug has been fixed with Firefox 45.
