---
title: "`<table>`'s size and position now take `<caption>` into account"
date: "2018-09-06T03:18:00-04:00"
categories: ["css", "dom"]
tags: []
releases: ["63", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=820891"
      title: "Bug 820891 - Table's caption element not taken into account for table's offsetTop and offsetHeight values"
---
Previously, the `<table>` element's `offset*`, `client*`, `scroll*` property values were excluding these values on the child `<caption>` element, which means only `<thead>`, `<tbody>` and `<tfoot>` were taken into account. For example, if `<caption>`'s `clientHeight` was `20` and `<tbody>`'s `clientHeight` was `80`, `<table>`'s `clientHeight` would be `80`, not `100`.

Firefox 63 has updated the implementation to match the current CSSOM spec and other browsers' behaviour, so the result of the example will be `100`. This change may break existing code if it has special handling for Firefox to calculate expected values.
