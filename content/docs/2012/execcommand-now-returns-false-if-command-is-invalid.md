---
title: "`execCommand()` now returns `false` if command is invalid"
date: "2012-10-09T06:00:00-04:00"
categories: ["dom"]
tags: []
versions: ["16"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=760052"
      title: "Bug 760052 – execCommand() should return false if the command isn’t enabled"
---
The [`document.execCommand`](https://developer.mozilla.org/docs/Web/API/document/execCommand) method used on [rich-text editors](https://developer.mozilla.org/docs/Rich-Text_Editing_in_Mozilla) now correctly returns `false` if the specified command is not valid. Previously it always returned `true`.
