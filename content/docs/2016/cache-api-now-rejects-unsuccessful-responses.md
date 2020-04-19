---
title: "Cache API now rejects unsuccessful responses"
date: "2016-02-05T15:09:00-05:00"
categories: ["dom"]
tags: []
releases: ["46", "52-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1244764"
      title: "Bug 1244764 - Cache .add() and .addAll() should reject if any response is not ok()"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/RbeEXAQ-yNQ/discussion"
      title: "mozilla.dev.platform - Heads Up: Cache API .add()/.addAll() non-backward compatible change"
---
Previously, the [`Cache.add`](https://developer.mozilla.org/docs/Web/API/Cache/add) and [`Cache.addAll`](https://developer.mozilla.org/docs/Web/API/Cache/addAll) methods were storing `4xx` and `5xx` error responses from [`fetch`](https://developer.mozilla.org/docs/Web/API/Globalfetch/fetch). This behaviour had confused developers, therefore the spec has been changed to reject any responses with a non-`2xx` HTTP status code where the [`Response.ok`](https://developer.mozilla.org/docs/Web/API/Response/ok) property becomes `false`, and raise a `TypeError`. Firefox 46 and later follow the updated spec.

As a side effect, those methods will always reject [`opaque`](https://developer.mozilla.org/docs/Web/API/Response/type) responses returned as the result of [`no-cors`](https://developer.mozilla.org/docs/Web/API/Request/mode) cross-origin requests, because such responses have the `0` status code instead of the actual code. This is a rare case at this moment according to the Blink team.
