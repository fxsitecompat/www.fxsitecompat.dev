---
title: "Non-standard `text` event will no longer be fired during IME composition"
date: "2018-11-30T02:45:00-05:00"
categories: ["dom"]
tags: []
versions: ["65", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1288640"
      title: "Bug 1288640 - Stop dispatching \"text\" event in web contents"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/2pw2HxiCIbc/discussion"
      title: "Intent to unship: DOM \"text\" event"
---
The non-standard `text` DOM event is no longer dispatched on web content as of Firefox 65. It was implemented to notify the browser's editor UI of the input method editor (IME) composition string data and selection range, which was intended only for internal use. Given that it's undocumented and supported by no other browsers, the compatibility risk should be very low.
