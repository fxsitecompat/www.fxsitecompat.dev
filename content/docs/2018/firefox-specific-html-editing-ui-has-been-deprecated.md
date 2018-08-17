---
title: "Firefox-specific HTML editing UI has been deprecated"
date: "2018-08-17T13:28:00-04:00"
categories: ["html"]
tags: []
versions: ["63"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1449564"
      title: "Bug 1449564 - Disable table/image resizers in default"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/6GDK3Kzu9q0/discussion"
      title: "Intent to disable (hide) Gecko specific editing UI of HTML editor by default"
---
The following editing UI features on the [HTML rich-text editor](https://developer.mozilla.org/docs/Web/Guide/HTML/Editable_content), only implemented in Firefox so far, are now considered deprecated and disabled by default in Firefox Nightly and early Beta/DevEdition as of Firefox 63. Assuming no major issues arise, these features will be removed from all the channels with Firefox 64.

1. object resizing on `<img>`, `<table>` and absolute-positioned elements
2. inline table editing to add or remove rows and columns
3. grabber for absolute-positioned elements

Currently, 1 and 2 can be disabled with the `enableObjectResizing` and `enableInlineTableEditing` commands for the [`document.execCommand`](https://developer.mozilla.org/docs/Web/API/Document/execCommand) method. There's no way to disable 3.
