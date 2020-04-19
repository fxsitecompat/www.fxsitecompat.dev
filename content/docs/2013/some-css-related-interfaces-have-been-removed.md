---
title: "Some CSS-related interfaces have been removed"
date: "2013-10-08T20:15:35-04:00"
categories: ["dom"]
tags: []
releases: ["27", "31-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=872934"
      title: "Bug 872934 – convert style sheet change event interfaces to Web IDL and stick [NoInterfaceObject] on them"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=916871"
      title: "Bug 916871 – Remove classinfo bits for CSSGroupRuleRuleList"
---
As part of the ongoing effort to standardize global objects, the non-standard stylesheet change event interfaces, including `StyleRuleChangeEvent`, `StyleSheetApplicableStateChangeEvent` and `StyleSheetChangeEvent`, are no longer available from Web content. The `CSSGroupRuleRuleList` interface, the implementation detail of [`CSSRuleList`](https://developer.mozilla.org/docs/Web/API/CSSRuleList), has also been removed.
