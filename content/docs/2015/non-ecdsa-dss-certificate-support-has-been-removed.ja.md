---
title: "ECDSA を使用していない DSS 証明書への対応が廃止されました"
date: "2015-01-16T09:37:54-05:00"
categories: ["privacy-security"]
tags: []
versions: ["37"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1073867"
      title: "Bug 1073867 – Remove support for DSS (non-ECC DSA) signatures from mozilla::pkix"
---
楕円曲線デジタル署名アルゴリズム (ECDSA) を使用していない Digital Signature Standard (DSS) に基づく証明書は Firefox やその他の Mozilla 製品では使用できなくなりました。
