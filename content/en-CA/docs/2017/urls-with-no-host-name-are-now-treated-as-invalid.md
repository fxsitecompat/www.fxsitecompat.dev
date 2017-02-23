---
title: "URLs with no host name are now treated as invalid"
date: "2017-02-22T20:24:00-05:00"
categories: ["html", "networking"]
tags: []
versions: ["54"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1275746"
      title: "Bug 1275746 - Don't allow empty host name for URLTYPE_AUTHORITY URLs"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1305204"
      title: "Bug 1305204 - When trying to send/reply/forward an e-mail on webmail.earthlink.net I get a message \"Please enter a URL\""
---
Firefox 54 and later will treat URLs without any host name, such as `http:`, `http://`, `ftp:` and `ftp://`, as invalid URLs where they're supposed to be. That means the following JavaScript code will now throw a `TypeError`:

```js
new URL('http://')
```

Also, HTML forms containing a URL-type input control like this will not be validated unless the value is changed manually or dynamically:

```html
<input type="url" value="http://">
```

In this case, you can replace the `value` attribute with `placeholder` to work around the issue.
