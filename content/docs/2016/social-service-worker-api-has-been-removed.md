---
title: "Social Service Worker API has been removed"
date: "2016-08-15T16:46:00-04:00"
categories: ["misc"]
tags: []
versions: ["48"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=898706"
      title: "Bug 898706 - [meta] Remove social FrameWorker"
---
The non-standard [Social Service Worker API](https://developer.mozilla.org/en-US/docs/Mozilla/Projects/Social_API/Service_worker_API_reference), a part of the Firefox-specific [Social API](https://developer.mozilla.org/en-US/docs/Mozilla/Projects/Social_API), has been removed with Firefox 48. Use the standard [Service Worker API](https://developer.mozilla.org/en-US/docs/Web/API/Service_Worker_API) instead. Note that the Social API itself has been [removed with Firefox 51](https://www.fxsitecompat.com/en-CA/docs/2016/social-api-has-been-removed-except-the-sharing-functionality/) except the sharing functionality.
