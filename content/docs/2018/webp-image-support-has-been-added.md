---
title: "WebP image support has been added"
date: "2018-11-15T09:40:00-05:00"
categories: ["misc"]
tags: []
versions: ["65"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1294490"
      title: "Bug 1294490 - Implement WebP image support"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1503653"
      title: "Bug 1503653 - Enable WebP image support by default"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/ywu0gzoQfRY/discussion"
      title: "Intent to implement and ship: WebP image support"
---
Firefox 65 has added the support for the [WebP image format](https://en.wikipedia.org/wiki/WebP) developed by Google. While it has been supported by Chrome and Opera for more than 5 years, Mozilla stopped the earlier implementation work due to several concerns over the new format. However, Firefox developers has had to alter their stance, because Microsoft Edge has recently added the support, and the number of broken sites only serving WebP images continues increasing.

If your site uses different image formats based on browser detection, it has to be updated so WebP will be served to Firefox 65 and later. Firefox will send `image/webp,*/*` as the default `Accept` HTTP request header for images, which is a recommended way to determine whether you serve WebP. It should be noted that Firefox 60 [Extended Support Release](https://www.mozilla.org/firefox/organizations/) (ESR), an older release that doesn't support the new format, will be available until October 2019.
