---
title: "1024 ビット未満の脆弱な署名を使用した RSA 証明書は受け付けなくなりました"
date: "2014-07-22T05:06:26-04:00"
categories: ["privacy-security"]
tags: []
versions: ["33"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=360126"
      title: "Bug 360126 – Stop accepting certificates that use RSA 1023 or weaker signatures"
---
RSA 512、1000、1023 ビットの証明書は、安全性が十分でないことから、Firefox によってブロックされるようになりました。現在発行されている証明書の大半は 2048 ビットの鍵長を持っているはずです。
