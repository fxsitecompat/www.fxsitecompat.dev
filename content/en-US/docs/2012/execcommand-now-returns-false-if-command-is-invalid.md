---
title: "`execCommand()` now returns `false` if command is invalid"
date: "2012-10-09T06:00:00-04:00"
categories: ["dom"]
tags: []
versions: "16"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=760052": "Bug 760052 – execCommand() should return false if the command isn’t enabled"
---
The `execCommand` method on [rich-text editors](https://developer.mozilla.org/en-US/docs/Rich-Text_Editing_in_Mozilla) now correctly returns `false` if the specified command is not valid. Previously it always returned `true`.
