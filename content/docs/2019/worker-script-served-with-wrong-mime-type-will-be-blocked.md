---
title: "Worker script served with wrong MIME type will be blocked"
date: "2019-05-13T04:06:00-04:00"
categories: ["dom", "javascript", "privacy-security"]
tags: []
versions: ["67"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1514680"
      title: "Bug 1514680 - Consider strictly enforcing MIME checks for `importScripts()`."
---
Starting with Firefox 67, for security reasons, worker scripts served with a wrong MIME type can no longer be loaded into a worker scope using the `importScripts` method. A similar change has already been made in [Firefox 51](https://www.fxsitecompat.com/en-CA/docs/2016/javascript-served-with-wrong-mime-type-will-be-blocked/) for regular JavaScript files. Make sure your script files are always served with `text/javascript` or `application/javascript`.
