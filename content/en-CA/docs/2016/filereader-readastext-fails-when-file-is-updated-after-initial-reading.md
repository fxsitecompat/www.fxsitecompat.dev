---
title: "`FileReader.readAsText` fails when file is updated after initial reading"
date: "2016-04-06T18:19:00-04:00"
categories: ["dom"]
tags: []
versions: ["45"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1260606"
      title: "Bug 1260606 - FileReader.readAsText(HTML_FORM_INPUT.files[0]) fails on content size change"
---
Firefox 45 has introduced a regression where the [`FileReader.readAsText`](https://developer.mozilla.org/en-US/docs/Web/API/FileReader/readAsText) method raises an error when trying to re-read a file that has been modified after it was initially read by the same [`FileReader`](https://developer.mozilla.org/en-US/docs/Web/API/FileReader) instance. This issue doesn't occur if the file size has not changed. Mozilla developers are working on the solution.
