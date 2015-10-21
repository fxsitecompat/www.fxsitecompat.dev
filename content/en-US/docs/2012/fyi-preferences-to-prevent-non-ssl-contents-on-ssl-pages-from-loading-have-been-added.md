---
title: "FYI: Preferences to prevent non-SSL contents on SSL pages from loading have been added"
date: "2012-12-03T03:53:26-05:00"
categories: ["privacy-security"]
tags: []
versions: ["18"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=62178": "Bug 62178 – implement mechanism to prevent sending insecure requests from a secure context"
---
2 preferences have been added to block loading contents from non-SSL (`http`) sites on SSL (`https`) pages. Scripts, stylesheets, plug-in contents, inline frames, [Web fonts](https://developer.mozilla.org/en-US/docs/Web/CSS/@font-face) and [WebSockets](https://developer.mozilla.org/en-US/docs/WebSockets) can be blocked with `security.mixed_content.block_active_content`, and other static contents like images, [audios](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/audio) and [videos](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/video) can be blocked with `security.mixed_content.block_display_content`.

Though both are disabled (`false`) by default for now, such contents won't be loaded if a user enables those preferences. Note that the former preference `security.mixed_content.block_active_content` will be [enabled by default](https://bugzilla.mozilla.org/show_bug.cgi?id=834836) in a future version of Firefox. Webmasters should make sure not to mix non-SSL contents on SSL pages.
