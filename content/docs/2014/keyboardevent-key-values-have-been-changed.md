---
title: "`KeyboardEvent.key` values have been changed"
date: "2014-02-07T11:57:09-05:00"
categories: ["dom"]
tags: []
versions: ["29"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=912858"
      title: "Bug 912858 – Implement KeyboardEvent.key for printable keys (except dead key handling)"
---
The [`KeyboardEvent.key`](https://developer.mozilla.org/docs/Web/API/KeyboardEvent.key) implementation has been updated for the latest DOM3 Events spec, and key values have been changed accordingly. For example, `"Spacebar"` becomes `" "` while `"Add"` becomes `"+"`. Also, printable, generic keys now return the actual characters instead of `"MozPrintableKey"`. Read [the document](https://developer.mozilla.org/docs/Web/API/KeyboardEvent.key) for details.

Note that the legacy [`KeyboardEvent.charCode`](https://developer.mozilla.org/docs/Web/API/KeyboardEvent.charCode), [`KeyboardEvent.keyCode`](https://developer.mozilla.org/docs/Web/API/KeyboardEvent.keyCode) and [`KeyboardEvent.which`](https://developer.mozilla.org/docs/Web/API/KeyboardEvent.which) properties are deprecated, and developers should consider using `KeyboardEvent.key` once the spec and implementation become stable.
