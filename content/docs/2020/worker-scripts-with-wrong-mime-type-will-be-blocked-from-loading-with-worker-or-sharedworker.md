---
title: "Worker scripts with wrong MIME type will be blocked from loading with `Worker()` or `SharedWorker()`"
date: "2020-02-17T15:07:00-04:00"
categories: ["dom", "javascript", "privacy-security"]
tags: []
versions: ["75"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1523706"
      title: "Bug 1523706 - Consider strictly enforcing MIME checks for Worker scripts"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1569122"
      title: "Bug 1569122 - Limit Worker/SharedWorker MIME type blocking to Beta/Nightly"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1569123"
      title: "Bug 1569123 - Re-enable strict MIME type checking for Worker/SharedWorker"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1583657"
      title: "Bug 1583657 - Worker with type \"application/octet-stream\" is blocked on color.adobe.com"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/EJ9EDv8bqxI/discussion"
      title: "Intent to ship: Blocking Worker/SharedWorker with non-JS MIME type"
aliases:
    - "/en-CA/docs/2019/worker-scripts-with-wrong-mime-will-be-blocked-from-loading-with-worker-or-sharedworker/"
    - "/en-CA/docs/2019/worker-scripts-with-wrong-mime-type-will-be-blocked-from-loading-with-worker-or-sharedworker/"
    - "/en-CA/docs/2019/worker-scripts-with-wrong-mime-type-will-be-blocked-from-loading-with-worker-or-sharedworker-in-nightly-and-early-beta/"
---
Starting with Firefox 75, for security reasons, dedicated and shared worker scripts served with a wrong MIME type will be blocked from loading with `Worker()` and `SharedWorker()` respectively. The change has already been made to the Nightly and early Beta channels since Firefox 70, and only one compatibility issue has been reported so far.

The same change has already been made in [Firefox 67](https://www.fxsitecompat.dev/en-CA/docs/2019/worker-scripts-with-wrong-mime-type-will-be-blocked-from-loading-with-importscripts/) to scripts loaded with `importScripts()`. Make sure your script files are always served with `text/javascript` or `application/javascript`.
