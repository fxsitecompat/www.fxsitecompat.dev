---
title: "ICO images now use the largest frame as the intrinsic dimention"
date: "2015-09-25T03:09:00-04:00"
categories: ["misc"]
tags: []
versions: "44"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1201796": "Bug 1201796 - Add downscale-during-decode support for the ICO decoder"
---
Previously, the dimention of ICO format images (favicons) with multiple frames was based on the smallest frame, which is usually 16×16px. Starting with Firefox 44, the largest frame is used instead as the intrinsic image dimention. 

While this change should not negatively affect the browser's UI including tabs and bookmarks, ICO images embedded on a Web page, using `<img>` elements, CSS `background-image` or other properties, might be displayed in different sizes unless the the `width` and `height` are set.
