---
title: "JavaScript served with wrong MIME type will be blocked"
date: "2016-09-07T01:38:00-04:00"
categories: ["javascript", "privacy-security"]
tags: []
versions: ["51"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1288361"
      title: "Bug 1288361 - Return a network error for requests whose type is \"script\" and response has a MIME type that starts with image/"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1299267"
      title: "Bug 1299267 - Return a network error for requests whose type is \"script\" with additional bad MIME types"
---
On Firefox 51 and later, JavaScript files served with a wrong MIME type such as `image/*`, `audio/*`, `video/*` or `text/csv` will not be loaded for security reasons, raising a `NetworkError`. The HTML `<script>` element, `new Worker()`, `new SharedWorker()` as well as the [`importScripts`](https://developer.mozilla.org/en-US/docs/Web/API/WorkerGlobalScope/importScripts) method are all affected. Make sure your script is served with an appropriate type such as `text/javascript` or `application/javascript`.
