---
title: "Dedicated workers no longer inherit CSP from parent document unless embedded"
date: "2016-03-13T11:59:00-04:00"
categories: ["dom", "privacy-security"]
tags: []
versions: ["45"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1223647"
      title: "Bug 1223647 - CSP erroneously \"inherited\" into dedicated workers"
---
Firefox 45 has fixed a [Content Security Policy](https://developer.mozilla.org/docs/Web/Security/CSP) (CSP) implementation bug where [dedicated workers](https://developer.mozilla.org/docs/Web/API/Web_Workers_API/Using_web_workers#Dedicated_workers) were erroneously "inheriting" the policy of the parent document when [`XMLHttpRequest`](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest) or [`importScripts`](https://developer.mozilla.org/docs/Web/API/WorkerGlobalScope/importScripts) was used.

In the meantime, [embedded workers](https://developer.mozilla.org/docs/Web/API/Web_Workers_API/Using_web_workers#Embedded_workers) do inherit the parent policy, but make sure your [`Blob`](https://developer.mozilla.org/docs/Web/API/Blob/Blob) has a valid script MIME type such as `text/javascript`. Otherwise, the `default-src` directive is applied to the worker instead of `script-src`, potentially leading to an unexpected CSP error. [*Yandex.Disk* is broken on Firefox 45](https://bugzilla.mozilla.org/show_bug.cgi?id=1256148) due to this restriction.

**Update**: The issue on *Yandex.Disk* has been solved by the Yandex team.
