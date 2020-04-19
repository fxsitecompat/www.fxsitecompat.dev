---
title: "Form validation no longer runs on hidden `<input>` elements"
date: "2017-03-10T13:42:00-05:00"
categories: ["dom", "html"]
tags: []
versions: ["53", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1319078"
      title: "Bug 1319078 - Form validation should account for the visibility/focusability of the input element"
---
Firefox 53 and later takes the visibility of input controls into account when running [form validation](https://developer.mozilla.org/docs/Learn/HTML/Forms/Data_form_validation), like Google Chrome. Unfocusable `<input>` elements hidden with `visibility:hidden` or `display:none`, for example, will be simply ignored even if the current value is actually invalid.
