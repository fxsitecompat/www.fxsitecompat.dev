---
title: "Media query resolutions are now calculated in CSS pixel unit"
date: "2012-10-09T06:00:00-04:00"
categories: ["css"]
tags: []
versions: ["16"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=771390"
      title: "Bug 771390 – [css3-mediaqueries] resolution units (dpi, dpcm, dppx) should be dots per CSS inch/centimeter/pixel, not per physical in/cm/px"
---
The [CSS3 Media Queries](https://developer.mozilla.org/docs/Web/CSS/Media_Queries) spec has been updated, and [resolution units](https://developer.mozilla.org/docs/Web/CSS/resolution), such as `dpi`, `dpcm` and `dppx`, now correspond to dots per CSS pixel instead of physical units. The Firefox implementation has been updated accordingly.
