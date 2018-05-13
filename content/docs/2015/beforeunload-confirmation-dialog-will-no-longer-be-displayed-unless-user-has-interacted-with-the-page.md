---
title: "`beforeunload` confirmation dialog will no longer be displayed unless user has interacted with the page"
date: "2015-09-29T10:25:00-04:00"
categories: ["dom"]
tags: []
versions: ["44"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=636905"
      title: "Bug 636905 - Don't allow onbeforeunload dialog unless I have interacted with the page"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=578828"
      title: "Bug 578828 - Default to not allowing onbeforeunload dialogs"
aliases:
    - "/en-CA/docs/2015/beforeunload-event-will-no-longer-be-fired-unless-user-has-interacted-with-the-page/"
    - "/en-CA/docs/2015/beforeunload-dialog-will-no-longer-be-displayed-unless-user-has-interacted-with-the-page/"
---
The [`beforeunload`](https://developer.mozilla.org/docs/Web/Events/beforeunload) event is sometimes misused to prevent Web pages, including popup ads, from being closed by users. Firefox now ignores the return value of `beforeunload` event handlers and forces page navigation without showing the confirmation dialog, unless the user has interacted with the page by clicking, touching, scrolling or typing on the elements.

There is also a plan to disallow all `beforeunload` dialogs by default, therefore Web developers are encouraged to avoid using this type of events to confirm page navigation. Web pages and apps can improve user experience while preventing dataloss by saving draft state locally with the [Web Storage API](https://developer.mozilla.org/docs/Web/API/Web_Storage_API) or [IndexedDB API](https://developer.mozilla.org/docs/Web/API/IndexedDB_API), or remotely with [Ajax](https://developer.mozilla.org/docs/Ajax) techniques.

**Update**: The initial draft of this document was misleading. The `beforeunload` event itself will still be fired even if the user has not interacted with the page.
