---
title: "`view-source:` URLs can no longer be linked from Web pages"
date: "2016-01-30T20:41:00-05:00"
categories: ["privacy-security"]
tags: []
versions: ["47"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1172165"
      title: "Bug 1172165 - Don't let web pages link to view-source: URLs"
---
For security reasons, Firefox now blocks links from Web pages to any `view-source:` URLs, that can be used to [view the source](https://developer.mozilla.org/en-US/docs/Tools/View_source) of an HTML or XML document, like other privileged URLs. On Firefox 47 and later, clicking on a `view-source:` URL just logs a `URI_DANGEROUS_TO_LOAD` exception in the Web Console.
