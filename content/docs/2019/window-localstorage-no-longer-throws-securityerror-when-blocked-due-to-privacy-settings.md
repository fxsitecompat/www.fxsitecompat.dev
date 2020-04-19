---
title: "`window.localStorage` no longer throws `SecurityError` when blocked due to privacy settings"
date: "2019-05-13T02:15:00-04:00"
categories: ["dom", "privacy-security"]
tags: []
versions: ["67", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1529396"
      title: "Bug 1529396 - Consider relaxing the exception-throwing semantics of window.localStorage when a privacy check fails"
---
Previously, `window.localStorage` was throwing a `SecurityError` exception when it's not available because of the user's privacy settings, specifically when cookies were disabled. On Firefox 67 and later, the property will be simply `null` in such cases, preventing certain websites from failing to load when a graceful `try-catch` handling is missing in JavaScript.

```js
// Note that this still throws a TypeError
// when window.localStorage becomes null
window.localStorage.setItem(key, value);

// So it has to be:
const storage = window.localStorage;

if (storage) {
  // Use storage
  storage.setItem(key, value);
}
```

**Update**: This change has been reverted with Firefox 70 due to the compatibility concerns. `window.localStorage` will throw a `SecurityError` again.
