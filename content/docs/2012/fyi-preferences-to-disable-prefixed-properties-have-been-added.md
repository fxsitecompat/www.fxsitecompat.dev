---
title: "FYI: Preferences to disable prefixed properties have been added"
date: "2012-12-03T03:54:45-05:00"
categories: ["css"]
tags: []
versions: ["19"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=804944"
      title: "Bug 804944 – add preferences for sets of CSS prefixed properties"
---
While this is not a change affecting site compatibility, it's worth mentioning because this has been developed as part of efforts to keep compatibility. Preferences to disable some major prefixed properties have been added: `layout.css.prefixes.border-image`, `layout.css.prefixes.transforms`, `layout.css.prefixes.transitions` and `layout.css.prefixes.animations`. Web developers can disable those preferences (change the values to `false`) to test whether style rules are applied as intended even after those prefixed implementations are removed. See [the David Baron's blog post](https://dbaron.org/log/20130225-removing-prefixes) for details.
