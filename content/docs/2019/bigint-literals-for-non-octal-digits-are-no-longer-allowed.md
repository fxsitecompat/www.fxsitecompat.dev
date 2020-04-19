---
title: "`BigInt` literals for non-octal digits are no longer allowed"
date: "2019-08-13T15:41:00-04:00"
categories: ["javascript"]
tags: []
releases: ["70"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1568619"
      title: "Bug 1568619 - Disallow BigInt literals for Annex-B non-octal digits"
---
On Firefox 70 and later, [`BigInt` literals](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Lexical_grammar#BigInt_literal) for non-octal digits such as `08n` or `09n` will be disallowed, raising a `SyntaxError`. The `BigInt` support was enabled recently in Firefox 68, so the compatibility risk should be very low.
