---
title: "EV SSL certs with a shorter key length are no longer accepted"
date: "2014-12-19T11:15:21-05:00"
categories: ["privacy-security"]
tags: []
versions: ["36", "38-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=622859"
      title: "Bug 622859 – Reject EV certificates with key sizes below RSA 2048"
---
Extended Validation (EV) SSL certificates using RSA keys less than 2048 bits are violating the EV SSL Certificate Guidelines, therefore those certificates are no longer accepted by Firefox and other Mozilla products.
