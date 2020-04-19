---
title: "HTTP auth dialog can no longer be triggered by cross-origin images"
date: "2017-12-06T14:19:00-05:00"
categories: ["networking", "privacy-security"]
tags: []
releases: ["59", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1357835"
      title: "Bug 1357835 - Add a pref to disable HTTP Auth on 3rd party images"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1423146"
      title: "Bug 1423146 - Do not allow an auth prompt requested by an image resource loaded from cross-origin"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/o1rWz3k1IxU/discussion"
      title: "Intent to ship: Do not allow a http-auth prompt requested by an image resource loaded from a cross-origin"
---
Starting with Firefox 59, an image resource loaded from a different origin from the current page can no longer trigger an HTTP authentication dialog prompt, preventing user credentials being stolen if attackers were able to embed an arbitrary image to the victimized page.

This security measure was originally introduced with [Firefox 40](https://www.fxsitecompat.dev/en-CA/docs/2015/http-auth-dialog-can-no-longer-be-triggered-by-cross-origin-resources/) but soon backed out due to several compatibility issues. While cross-origin frames and scripts may still be used to trigger an auth dialog in some organizations, images are unlikely legit, hence the change. Given that Google Chrome has already implemented this, Mozilla developers expect nothing will be broken.
