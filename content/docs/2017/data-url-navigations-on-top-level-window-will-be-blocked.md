---
title: "Data URL navigations on top level window will be blocked"
date: "2017-09-20T22:02:00-04:00"
categories: ["dom", "privacy-security"]
tags: []
versions: ["59"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1331351"
      title: "Bug 1331351 - Consider blocking top level window data: URIs"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1380959"
      title: "Bug 1380959 - Block toplevel data: URI navigations in Nightly and early Beta"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1398692"
      title: "Bug 1398692 - Potentially allow navigations to toplevel data: PDFs"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1396798"
      title: "Bug 1396798 - Don't block top level data: URIs when loading an image"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1401895"
      title: "Bug 1401895 - Block top-level navigations to data: URIs"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1403641"
      title: "Bug 1403641 - Download behaviour for data: URL seems different in FF57 compared to 55"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1403814"
      title: "Bug 1403814 - Block toplevel data: URI navigations only if openend in the browser"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1403870"
      title: "Bug 1403870 - Potentially allow navigations to data:application/json"
---
[Data URLs](https://developer.mozilla.org/en-US/docs/Web/HTTP/Basics_of_HTTP/Data_URIs), URLs prefixed with the `data:` scheme allowing to embed small data files on web pages, are sometimes exploited for phishing attacks, because such kinds of URLs are able to contain a legitimate address string while showing disguised content in the browser.

In order to mitigate the security risk, Firefox will soon block navigation attempts that will otherwise open a data URL in the top level browser window. This change has already been made to the Nightly and early Beta channels including Developer Edition as of version 57, and affects the following scenarios:

* A data URL link on a page is clicked manually or programmatically
* A page tries to load a data URL with `location.href`, `location.assign()` or `location.replace()`
* A page tries to load a data URL in a new tab with `window.open()`
* A frame content tries to load a data URL in the top level window or in a new tab

Note that non-SVG images and PDF files are whitelisted so those data URL navigations are always allowed.

Meanwhile, these operations will *not* be affected:

* A user manually types a data URL in the Address Bar to tries to load the content
* A page tries to load a data URL in a `<frame>` or `<iframe>`
* A page uses a data URL for an image or other assets

**Update**: Firefox 58 Nightly and early Beta has updated the implementation so JSON files are also whitelisted, and data files that triggers the download will no longer be blocked.
