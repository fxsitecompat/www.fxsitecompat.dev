---
title: "Submitting empty file input control results in no `Content-Type`"
date: "2016-04-11T13:12:00-04:00"
categories: ["dom"]
tags: []
releases: ["45", "45-esr"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1255735"
      title: "Bug 1255735 - Firefox 45 does not send content-type in empty input[type=file] anymore"
---
Firefox 45 has introduced a regression where submitting a `<form enctype="multipart/form-data">` with an empty `<input type="file">` fails to send the `Content-Type` HTTP header as well as the `filename` field in the `Content-Disposition` header, potentially breaking the application's server-side logic while parsing the form data.

Actual:
```http
Content-Disposition: form-data; name="multipartFileList"
```

Expected:
```http
Content-Type: application/octet-stream
Content-Disposition: form-data; name="multipartFileList"; filename=""
```

This bug has been fixed with Firefox 45.0.2.
