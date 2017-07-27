---
title: "短い鍵長の EV SSL 証明書が受け入れられなくなりました"
date: "2014-12-19T11:15:21-05:00"
categories: ["privacy-security"]
tags: []
versions: ["36"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=622859"
      title: "Bug 622859 – Reject EV certificates with key sizes below RSA 2048"
---
2048 ビット未満の RSA 鍵を使用した Extended Validation (EV) SSL 証明書は EV SSL 証明書ガイドラインに違反しており、今後そうした証明書は Firefox やその他の Mozilla 製品では受け入れられなくなります。
