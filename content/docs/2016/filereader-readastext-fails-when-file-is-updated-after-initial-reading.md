---
title: "`FileReader.readAsText` fails when file is updated after initial reading"
date: "2016-04-06T18:19:00-04:00"
categories: ["dom"]
tags: []
versions: ["45"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1260606"
      title: "Bug 1260606 - FileReader.readAsText(HTML_FORM_INPUT.files[0]) fails on content size change"
---
Firefox 45 has introduced a regression where the [`FileReader.readAsText`](https://developer.mozilla.org/en-US/docs/Web/API/FileReader/readAsText) method raises an error when trying to re-read a file that has been modified since it was initially read. This issue doesn't occur if the file size has not changed. Mozilla developers are working on the solution.

**Update**: According to the discussion in the bug, this behaviour is considered not a regression because the spec says [`File`](https://developer.mozilla.org/en-US/docs/Web/API/File) objects are immutable and re-reading a modified file should always fail. To work around the issue, you should always use a new [`FileReader`](https://developer.mozilla.org/en-US/docs/Web/API/FileReader) instance to read a file.
