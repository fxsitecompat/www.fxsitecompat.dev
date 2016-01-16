---
title: "Table cell heights are now calculated properly regardless of the border"
date: "2012-10-09T06:00:00-04:00"
categories: ["css"]
tags: []
versions: ["16"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=248239": "Bug 248239 – borders and padding on the top and bottom of table cells reduce the height"
---
Previously, table cells or [`<td>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/td) elements were shrunken if a `border` or `padding` was specified at the top or bottom of the cell. Firefox 16 has fixed this layout issue to comply with the CSS spec. See the test cases in the bug for actual examples.
