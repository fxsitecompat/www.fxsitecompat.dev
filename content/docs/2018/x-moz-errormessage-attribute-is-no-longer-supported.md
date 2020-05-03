---
title: "`x-moz-errormessage` attribute is no longer supported"
date: "2018-12-25T00:08:00-05:00"
categories: ["html"]
tags: []
releases: ["66", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1513890"
      title: "Bug 1513890 - Remove 'x-moz-errormessage' attribute"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/LDNiOssSN3U/discussion"
      title: "Intent to unship: x-moz-errormessage attribute"
supported_tools:
  firefox_extension: true
---
Firefox 66 has dropped the support for the non-standard `x-moz-errormessage` attribute for the HTML `<input>` element that allowed to specify a custom error message to display when the [form validation](https://developer.mozilla.org/docs/Learn/HTML/Forms/Form_validation) failed. The standard [`setCustomValidity`](https://developer.mozilla.org/docs/Web/API/HTMLSelectElement/setCustomValidity) method can be used instead.
