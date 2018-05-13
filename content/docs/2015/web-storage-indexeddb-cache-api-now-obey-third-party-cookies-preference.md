---
title: "Web Storage, IndexedDB, Cache API now obey third-party cookies preference"
date: "2015-10-24T16:10:00-07:00"
categories: ["dom", "privacy-security"]
tags: []
versions: ["43"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=536509"
      title: "Bug 536509 - localStorage does not obey \"third-party cookies\" pref"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1147821"
      title: "Bug 1147821 - Only disable IndexedDB in third-party windows when the third-party cookie preference is set"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1145744"
      title: "Bug 1145744 - Disallow Cache API in 3rd party windows when 3rd party cookies are disabled"
---
The [Web Storage API](https://developer.mozilla.org/docs/Web/API/Web_Storage_API) now respects the browser's third-party cookies preference, so it will no longer work when the script is in a third-party context and the user has [disabled third-party cookies](https://support.mozilla.org/kb/disable-third-party-cookies). The [IndexedDB API](https://developer.mozilla.org/docs/Web/API/IndexedDB_API) and the new [Service Worker Cache API](https://developer.mozilla.org/docs/Web/API/Cache) will also obey the same constraint.
