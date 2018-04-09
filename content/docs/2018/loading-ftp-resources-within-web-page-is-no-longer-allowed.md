---
title: "Loading FTP resources within web page is no longer allowed"
date: "2018-04-06T20:32:00-04:00"
categories: ["dom", "privacy-security"]
tags: []
versions: ["61"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1404744"
      title: "Bug 1404744 - Block ftp subresource requests inside http(s) pages"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/HzumeW2JQW8/discussion"
      title: "Intent to implement and ship: Blocking FTP subresources"
---
Firefox 61 and later will block HTTP(S) pages from loading resources from FTP servers. This security measure typically affects `<img>`, `<script>` and `<iframe>` elements with `src="ftp://..."`. Those FTP resources can still be loaded if opened directly within the browser or any FTP page, and links to FTP servers are also not blocked. Given that [Google Chrome](https://www.chromestatus.com/feature/5709390967472128) has already made the change with the version 59 shipped in June 2017, the compatibility risk should be low.

The FTP support in Firefox might be deprecated in the future because of the insecurity, but there's no concrete schedule at this time.
