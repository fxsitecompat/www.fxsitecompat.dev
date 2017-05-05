---
title: "Form validation error messages disappear quickly"
date: "2017-04-24T00:42:00-04:00"
categories: ["dom", "html"]
tags: []
versions: ["53"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1358487"
      title: "Bug 1358487 - Native form validation error messages do not appear"
---
Firefox 53 has introduced a regression where the browser's native [form data validation](https://developer.mozilla.org/en-US/docs/Learn/HTML/Forms/Form_validation) error messages will disappear in an instant, making it difficult for users to understand what's wrong with their input. This issue has already been fixed with Firefox 54 Beta. A minor update for Firefox 53, if any, may also contain the patch.

**Update**: This issue has been fixed with Firefox 53.0.2.
