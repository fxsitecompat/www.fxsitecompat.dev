---
title: "Images are not updated in some cases when `srcset` is modified"
date: "2016-03-24T15:26:00-04:00"
categories: ["dom"]
tags: []
versions: ["45"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1259482"
      title: "Bug 1259482 - Product image not changing upon selection in Woocommerce/Wordpress"
---
Firefox 45 has introduced a regression where [responsive images](https://developer.mozilla.org/en-US/Learn/HTML/Multimedia_and_embedding/Responsive_images) with the [`srcset`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/img#attr-srcset) attribute, introduced with Firefox 38, fail to get updated when the attribute value is programmatically changed in a certain way. This bug is affecting product image display on *WooCommerce*-powered online stores. Mozilla developers are working on the solution.
