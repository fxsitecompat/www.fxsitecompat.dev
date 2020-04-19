---
title: "一部の暗号スイートが無効化されました"
date: "2014-07-22T05:06:26-04:00"
categories: ["privacy-security"]
tags: []
versions: ["33", "38-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1036765"
      title: "Bug 1036765 – Disable cipher suites that are not in the \"Browser Cipher Suite\" proposal that are still enabled"
---
一部の古い、安全でない、あるいはあまり使われていない暗号スイートが、[暗号スイート提案](https://groups.google.com/d/topic/mozilla.dev.tech.crypto/duNhREcIAe8) に沿って廃止予定とされ、標準で無効化されました。これには、3DES、Camellia、DSS、RC4 が含まれます。
