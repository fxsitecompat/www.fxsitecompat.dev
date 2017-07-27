---
title: "`HTMLTableElement.insertRow` now always inserts the row to `<tbody>`"
date: "2014-06-09T02:46:54-04:00"
categories: ["dom"]
tags: []
versions: ["32"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1003539"
      title: "Bug 1003539 – HTMLTableElement.insertRow doesn\'t insert the row at the right place when table has a thead or tfoot, no tbody, and no rows"
---
The behaviour of the [`HTMLTableElement.insertRow`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLTableElement.insertRow) method has been changed to follow the latest HTML5 spec. When there is a [`<thead>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/thead) but no [`<tbody>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/tbody) and [`<tr>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/tr), the new `<tr>` will be inserted to a newly created `<tbody>` instead of the existing `<thead>`.
