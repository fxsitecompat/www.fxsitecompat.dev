---
title: "`localStorage` quota has been limited to 5 MB"
date: "2012-12-03T03:53:26-05:00"
categories: ["dom"]
tags: []
versions: ["18"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=776416"
      title: "Bug 776416 – Remove exceptions to 5MB quota rule in localStorage"
---
Previously Web pages with the offline storage enabled can save the own data up to 200 MB. Unfortunately [`localStorage`](https://developer.mozilla.org/docs/Web/Guide/DOM/Storage#localStorage) causes performance issues as it requires synchronous IO. For that reason, the quota has been changed to 5 MB. Also, from now the data in a `localStorage` will be deleted at the same time user deletes Cookies. You're recommended to use the [`IndexedDB`](https://developer.mozilla.org/docs/IndexedDB) async API instead.
