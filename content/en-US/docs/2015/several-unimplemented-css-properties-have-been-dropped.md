---
title: "Several unimplemented CSS properties have been dropped"
date: "2015-10-20T16:23:00-07:00"
categories: ["css"]
tags: []
versions: ["44"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1215702": "Bug 1215702 - remove backend-only CSS properties (marks, orphans, page, size, widows)"
---
The support for the [`marks`](https://developer.mozilla.org/en-US/docs/Web/CSS/%40page/marks), [`orphans`](https://developer.mozilla.org/en-US/docs/Web/CSS/orphans), `page`, `size` and [`widows`](https://developer.mozilla.org/en-US/docs/Web/CSS/widows) properties has been removed. Those were parsed and cached but not computed because Firefox has not actually implemented them yet. The [`@supports`](https://developer.mozilla.org/en-US/docs/Web/CSS/@supports) at-rule and the [`CSS.supports`](https://developer.mozilla.org/en-US/docs/Web/API/CSS/supports) method will no longer work with those properties, but otherwise this change should not affect site compatibility.
