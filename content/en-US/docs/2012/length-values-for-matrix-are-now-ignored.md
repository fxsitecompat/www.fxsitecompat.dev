---
title: "Length values for `matrix()` are now ignored"
date: "2012-10-09T06:00:00-04:00"
categories: ["css"]
tags: []
versions: ["16"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=719054": "Bug 719054 – matrix() and matrix3d() with length units should be parse errors"
---
Previously, Firefox was incorrectly accepting length values, such as a value with a unit like `10px`, in addition to numeric values, for the `matrix` and `matrix3d` [transform functions](https://developer.mozilla.org/en-US/docs/Web/CSS/transform-function). This behavior has been fixed to comply with the spec so a parse error will be returned for length values.
