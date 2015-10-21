---
title: "Curly brackets are no longer allowed in `style` attributes"
date: "2013-10-08T20:15:35-04:00"
categories: ["css"]
tags: []
versions: ["27"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=915053": "Bug 915053 – remove quirk allowing {} around style attribute"
---
Previously, in Firefox [Quirks (backward compatibility) mode](https://developer.mozilla.org/en-US/docs/Mozilla_Quirks_Mode_Behavior), the CSS parser allowed curly brackets around the contents of `style` attributes like `<div style="{ color: blue; }">`. This behavior has been removed from Firefox 27 for interoperability.
