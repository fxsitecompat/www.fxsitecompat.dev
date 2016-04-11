---
title: "Images are not updated in some cases when `srcset` is dynamically changed"
date: "2016-03-24T15:26:00-04:00"
categories: ["dom"]
tags: []
versions: ["45"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1259482"
      title: "Bug 1259482 - Product image not changing upon selection in Woocommerce/Wordpress"
aliases:
    - "/docs/2016/images-are-not-updated-in-some-cases-when-srcset-is-modified/"
---
Firefox 45 has introduced a regression where [responsive images](https://developer.mozilla.org/en-US/Learn/HTML/Multimedia_and_embedding/Responsive_images) with the [`srcset`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/img#attr-srcset) attribute, introduced with Firefox 38, fail to get updated when the attribute value is programmatically changed in a certain way. This bug is affecting product image display on *WooCommerce*-powered online stores. Mozilla developers will be working on the solution.

**Update**: Our analysis has found that this bug affects the [*YITH WooCommerce Zoom Magnifier*](https://wordpress.org/plugins/yith-woocommerce-zoom-magnifier/) plugin that has 90,000+ active installs.

**Update**: Firefox 45.0.2 has been patched, but the QA team reports that the issue is still rarely reproducible. Mozilla developers are investigating the cause.
