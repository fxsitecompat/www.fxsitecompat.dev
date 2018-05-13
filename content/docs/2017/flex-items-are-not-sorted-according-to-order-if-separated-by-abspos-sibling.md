---
title: "Flex items are not sorted according to `order` if separated by abspos sibling"
date: "2017-03-14T20:13:00-04:00"
categories: ["css"]
tags: []
versions: ["52"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1345873"
      title: "Bug 1345873 - flex items aren't sorted according to \"order\", if they're separated by an abspos sibling"
---
On Firefox 52, the CSS [`order`](https://developer.mozilla.org/docs/Web/CSS/order) property, which allows to sort flex items by an arbitrary order, is ignored in some cases if those items are separated by an absolutely-positioned element like this:

```html
<div style="display:flex">
  <div style="order:2">B</div>
  <div style="position:absolute"></div>
  <div style="order:1">A</div>
</div>
```

Mozilla developers are aware of the regression and working on the solution.

**Update**: This issue has been fixed with Firefox 53 and Firefox ESR 52.1.
