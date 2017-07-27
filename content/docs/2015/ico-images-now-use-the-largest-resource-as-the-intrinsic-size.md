---
title: "ICO images now use the largest resource as the intrinsic size"
date: "2015-09-25T03:09:00-04:00"
categories: ["misc"]
tags: []
versions: ["43"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1201796"
      title: "Bug 1201796 - Add downscale-during-decode support for the ICO decoder"
aliases:
    - "/en-CA/docs/2015/ico-images-now-use-the-largest-frame-as-the-intrinsic-dimention/"
    - "/en-CA/docs/2015/ico-images-now-use-the-largest-frame-as-the-intrinsic-dimension/"
---
Previously, the dimension of ICO format images (favicons) with multiple resources was based on the smallest resource, which is usually 16×16px. Starting with Firefox 43, the largest resource will be used instead as the intrinsic image size.

While this change should not negatively affect the browser's UI including tabs and bookmarks, ICO images embedded on a Web page, using `<img>` elements, CSS `background-image` or other properties, might be displayed in different sizes unless the the `width` and `height` are set.
