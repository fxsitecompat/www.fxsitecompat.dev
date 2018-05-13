---
title: "Social Service Worker API が削除されました"
date: "2016-08-15T16:46:00-04:00"
categories: ["misc"]
tags: []
versions: ["48"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=898706"
      title: "Bug 898706 - [meta] Remove social FrameWorker"
---
Firefox 固有の [Social API](https://developer.mozilla.org/docs/Mozilla/Projects/Social_API) の一部であった非標準の [Social Service Worker API](https://developer.mozilla.org/docs/Mozilla/Projects/Social_API/Service_worker_API_reference) が Firefox 48 で削除されました。標準の [Service Worker API](https://developer.mozilla.org/docs/Web/API/Service_Worker_API) を代用してください。なお、Social API 自体、共有機能を除き [Firefox 51 で削除されています](https://www.fxsitecompat.com/ja/docs/2016/social-api-has-been-removed-except-the-sharing-functionality/)。
