---
title: "Some non-essential Flash plug-in content will be blocked"
date: "2016-08-20T16:36:00-04:00"
categories: ["plugins"]
tags: []
versions: ["49"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1275591"
      title: "Bug 1275591 - Enable plugin content blocking by default"
    - url: "https://blog.mozilla.org/futurereleases/2016/07/20/reducing-adobe-flash-usage-in-firefox/"
      title: "Reducing Adobe Flash Usage in Firefox"
---
As part of the ongoing [NPAPI plug-in deprecation](https://www.fxsitecompat.com/en-CA/docs/2015/plug-in-support-will-be-dropped-by-the-end-of-2016-except-flash/), Firefox has implemented a plug-in blocklist focused on non-essential Flash content, aiming to improve the performance, stability and security of the browser. The [blocklist](https://github.com/mozilla-services/shavar-plugin-blocklist), mainly containing invisible Flash pixels embedded on Web pages, is going to be expanded over time while taking care of site compatibility issues. See [this Future Releases blog post](https://blog.mozilla.org/futurereleases/2016/07/20/reducing-adobe-flash-usage-in-firefox/) for details.
