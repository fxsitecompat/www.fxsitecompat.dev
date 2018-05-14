---
title: "`formMethod` and `formEnctype` now take an empty string as default value"
date: "2013-02-06T08:44:10-05:00"
categories: ["dom"]
tags: []
versions: ["21"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=787095"
      title: "Bug 787095 – Update formMethod reflection to have the empty string as default value (and \'get\' as invalid value)"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=839171"
      title: "Bug 839171 – Update formMethod reflection to have the empty string as default value (and \'get\' as invalid value)"
---
The HTML5 spec of the [`formMethod`](https://developer.mozilla.org/docs/HTML/Element/Input#attr-formmethod) and [`formEnctype`](https://developer.mozilla.org/docs/HTML/Element/Input#attr-formenctype) properties has been updated to have the empty string as default value. Firefox followed the change.
