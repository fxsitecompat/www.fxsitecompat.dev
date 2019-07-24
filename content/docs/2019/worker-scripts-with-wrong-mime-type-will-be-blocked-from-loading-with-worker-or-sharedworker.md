---
title: "Worker scripts with wrong MIME type will be blocked from loading with `Worker()` or `SharedWorker()`"
date: "2019-07-24T07:00:00-04:00"
categories: ["dom", "javascript", "privacy-security"]
tags: []
versions: ["70"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1523706"
      title: "Bug 1523706 - Consider strictly enforcing MIME checks for Worker scripts"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/EJ9EDv8bqxI/discussion"
      title: "Intent to ship: Blocking Worker/SharedWorker with non-JS MIME type"
aliases:
    - "/en-CA/docs/2019/worker-scripts-with-wrong-mime-will-be-blocked-from-loading-with-worker-or-sharedworker/"
---
Starting with Firefox 70, for security reasons, dedicated and shared worker scripts served with a wrong MIME type will be blocked from loading with `Worker()` and `SharedWorker()` respectively. The same change has already been made in [Firefox 67](https://www.fxsitecompat.dev/en-CA/docs/2019/worker-scripts-with-wrong-mime-type-will-be-blocked-from-loading-with-importscripts/) to scripts loaded with `importScripts()`. Make sure your script files are always served with `text/javascript` or `application/javascript`.
