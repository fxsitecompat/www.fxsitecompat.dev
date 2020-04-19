---
title: "MIME types treated as JavaScript have increased"
date: "2012-12-03T03:50:54-05:00"
categories: ["javascript"]
tags: []
releases: ["17"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=672814"
      title: "Bug 672814 – Increase the set of script @type values that nsScriptLoader treats as JavaScript"
---
In Firefox, scripts with MIME type of other than `text/javascript`, `text/ecmascript`, `application/javascript`, `application/ecmascript` and `application/x-javascript` haven't been treated as JavaScript. For example, code like `<script type="text/jscript"> ... </script>` doesn't work on the previous versions of Firefox. Starting with Firefox 17, various MIME types including `text/jscript` are now supported to follow the HTML5 draft. This can lead to unexpected issues as scripts that haven't been executed will be executed.
