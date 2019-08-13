---
title: "非 8 進法数字の `BigInt` リテラルは許容されなくなりました"
date: "2019-08-13T15:41:00-04:00"
categories: ["javascript"]
tags: []
versions: ["70"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1568619"
      title: "Bug 1568619 - Disallow BigInt literals for Annex-B non-octal digits"
---
Firefox 70 以降、`08n` や `09n` といった非 8 進法数字の `BigInt` リテラルは禁止され、`SyntaxError` が投げられます。`BigInt` 対応は最近 Firefox 68 で有効化されたことから、互換性リスクは非常に低いはずです。
