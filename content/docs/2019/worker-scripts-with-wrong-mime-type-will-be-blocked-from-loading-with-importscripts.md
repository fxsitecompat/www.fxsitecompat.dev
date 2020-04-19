---
title: "Worker scripts with wrong MIME type will be blocked from loading with `importScripts()`"
date: "2019-05-13T04:06:00-04:00"
categories: ["dom", "javascript", "privacy-security"]
tags: []
releases: ["67", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1514680"
      title: "Bug 1514680 - Consider strictly enforcing MIME checks for `importScripts()`."
aliases:
    - "/en-CA/docs/2019/worker-script-served-with-wrong-mime-type-will-be-blocked/"
    - "/en-CA/docs/2019/worker-scripts-with-wrong-mime-will-be-blocked-from-loading-with-importscripts/"
---
Starting with Firefox 67, for security reasons, worker scripts served with a wrong MIME type can no longer be loaded into a worker scope using the `importScripts` method. A similar change has already been made in [Firefox 51](https://www.fxsitecompat.dev/en-CA/docs/2016/javascript-served-with-wrong-mime-type-will-be-blocked/) for regular JavaScript files. Make sure your script files are always served with `text/javascript` or `application/javascript`.

**Update**: [Firefox 75](https://www.fxsitecompat.dev/en-CA/docs/2020/worker-scripts-with-wrong-mime-type-will-be-blocked-from-loading-with-worker-or-sharedworker/) has applied the same change to worker scripts loaded with `Worker()` and `SharedWorker()`. The title of this post has been updated to clarify the change in Firefox 67 only applies to `importScripts()`.
