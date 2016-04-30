---
title: "`<input pattern>` now sets `u` flag for regular expressions"
date: "2016-04-30T11:13:00-04:00"
categories: ["html"]
tags: []
versions: ["46"]
statuses: "affected"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1227906"
      title: "Bug 1227906 - HTML `pattern` attribute should set `u` flag for regular expressions"
    - url: "https://stackoverflow.com/questions/36953775/firefox-error-unable-to-check-input-because-the-pattern-is-not-a-valid-regexp"
      title: "Firefox error: Unable to check input because the pattern is not a valid regexp: invalid identity escape in regular expression"
---
The `pattern` attribute on the [`<input>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input) element, introduced with HTML5, is used to check the entered value against the author-defined regular expression. Starting with Firefox 46, the new `u` flag, introduced with ECMAScript 2015 (ES6), is set for the expression according to the latest HTML spec, treating it as a sequence of Unicode code points. Therefore, an unnecessary or invalid escape in the pattern such as `[\@\%]` will raise a `SyntaxError` saying "invalid identity escape in regular expression" and the validation will fail.
