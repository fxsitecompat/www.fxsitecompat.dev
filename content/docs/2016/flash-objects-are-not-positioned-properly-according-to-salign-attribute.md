---
title: "Flash objects are not positioned properly according to `salign` attribute"
date: "2016-10-24T10:41:00-04:00"
categories: ["plugins"]
tags: []
releases: ["49"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1307694"
      title: "Bug 1307694 - Flash objects in Firefox 49 are not positioned according to the salign attribute"
---
Firefox 49 has introduced a regression where the `salign` [optional attribute](https://helpx.adobe.com/flash/kb/flash-object-embed-tag-attributes.html#main_Optional_attributes) for the `<object>` and `<embed>` elements was ignored, leading to an unexpected layout within certain Flash objects. This bug has been fixed with Firefox 50.
