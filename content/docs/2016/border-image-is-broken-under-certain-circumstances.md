---
title: "`border-image` is broken under certain circumstances"
date: "2016-12-01T01:58:00-05:00"
categories: ["css"]
tags: []
releases: ["50"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1315353"
      title: "Bug 1315353 - \"border-image: url(\"data:image/svg+xml\") repeat\" broken after implementation of space value of border-image-repeat"
---
Firefox 50 has introduced a regression where the [`border-image`](https://developer.mozilla.org/docs/Web/CSS/border-image) CSS property could be partially broken due to the misimplementation of the new `space` value for the [`border-image-repeat`](https://developer.mozilla.org/docs/Web/CSS/border-image-repeat) property. This bug has been fixed with Firefox 50.1.0.
