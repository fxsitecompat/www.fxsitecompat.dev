---
title: "Page is automatically closed when `window.open()` triggers file download"
date: "2017-06-20T19:43:00-04:00"
categories: ["dom"]
tags: []
versions: ["54"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1373109"
      title: "Bug 1373109 - [e10s] window.open closes source page automatically after"
---
Firefox 54 has introduced a regression where the current browser tab is unexpectedly closed if the [`window.open`](https://developer.mozilla.org/docs/Web/API/Window/open) method is used to download a file such as a PDF document or ZIP archive. Mozilla developers are working on the solution. Web developers are encouraged to specify the HTML5 `download` attribute on the `<a>` element to [create a download link](https://developer.mozilla.org/docs/Learn/HTML/Introduction_to_HTML/Creating_hyperlinks#Use_the_download_attribute_when_linking_to_a_download).
