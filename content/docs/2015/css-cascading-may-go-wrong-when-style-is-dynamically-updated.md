---
title: "CSS cascading may go wrong when style is dynamically updated"
date: "2015-10-04T22:08:00-04:00"
categories: ["css"]
tags: []
versions: ["41"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1209603"
      title: "Bug 1209603 - specific combinations of em units and dynamic style changes can cause incorrect values of font properties"
---
Firefox 41 has introduced a bug in the CSS cascading effect due to the enhanced style caching, where property values are wrongly calculated when the style is programmatically changed in a certain way. Given there is only one report so far, this issue likely occurs in very limited circumstances. Mozilla developers are working on the solution.

**Update**: This bug, likely reproduced only with font properties, has been fixed with Firefox 44.
