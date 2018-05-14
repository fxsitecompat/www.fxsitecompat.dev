---
title: "`<form autocomplete=\"off\">` no longer prevents passwords from being saved"
date: "2014-03-21T04:50:04-04:00"
categories: ["privacy-security"]
tags: []
versions: ["30"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=956906"
      title: "Bug 956906 – ignore autocomplete=\"off\" when offering to save passwords via the password manager"
---
Firefox has offered page authors an ability to [turn off the form autocompletion](https://developer.mozilla.org/docs/Web/Security/Securing_your_site/Turning_off_form_autocompletion) by setting the `autocomplete="off"` attribute to a [`<form>`](https://developer.mozilla.org/docs/Web/HTML/Element/form) or [`<input>`](https://developer.mozilla.org/docs/Web/HTML/Element/input) element. This feature now works the way it should be: the [Password Manager](https://support.mozilla.org/kb/password-manager-remember-delete-change-passwords) always prompts if the user wants to save the password, while the autofill can be disabled as usual. Internet Explorer and Chrome have also made similar changes.
