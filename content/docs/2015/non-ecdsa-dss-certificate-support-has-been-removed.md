---
title: "Non-ECDSA DSS certificate support has been removed"
date: "2015-01-16T09:37:54-05:00"
categories: ["privacy-security"]
tags: []
versions: ["37", "38-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1073867"
      title: "Bug 1073867 – Remove support for DSS (non-ECC DSA) signatures from mozilla::pkix"
---
Digital Signature Standard (DSS) based certificates that are not using the Elliptic Curve Digital Signature Algorithm (ECDSA) are no longer supported by Firefox and other Mozilla products.
