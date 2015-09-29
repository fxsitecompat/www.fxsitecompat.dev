---
title: "`beforeunload` event will no longer be fired unless user has interacted with the page"
date: "2015-09-29T10:25:00-04:00"
categories: ["dom"]
tags: []
versions: "44"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=636905": "Bug 636905 - Don't allow onbeforeunload dialog unless I have interacted with the page"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=578828": "Bug 578828 - Default to not allowing onbeforeunload dialogs"
---
The [`beforeunload`](https://developer.mozilla.org/en-US/docs/Web/Events/beforeunload) event is sometimes misused to show popup windows, especially with a hidden [`<iframe>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/iframe). To enhance the popup blocking functionality, Firefox now ignores `beforeunload` event handlers unless the user has interacted with the page by clicking, touching, scrolling or typing on the elements.

There is also a plan to disallow all `beforeunload` event handlers by default, therefore Web developers are encouraged to avoid using this type of events. Web pages and apps can improve user experience while preventing dataloss by saving draft state locally with the [Web Storage API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Storage_API) or [IndexedDB API](https://developer.mozilla.org/en-US/docs/Web/API/IndexedDB_API), or remotely with [Ajax](https://developer.mozilla.org/en-US/docs/Ajax) techniques.
