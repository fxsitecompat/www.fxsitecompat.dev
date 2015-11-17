---
title: "EV certs valid for more than 27 months will be treated as DV certs"
date: "2015-11-16T22:08:00-08:00"
categories: ["privacy-security"]
tags: []
versions: ["45"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1222903": "Bug 1222903 - Reject EV status for EV EE certs that are valid for longer than 27 months as well"
---
Starting from [Firefox 42](https://www.fxsitecompat.com/en-US/docs/2015/ev-certs-with-overly-long-validity-periods-will-be-treated-as-dv-certs/), EV certs valid for more than 39 months have been treated as DV certs. Firefox 45 has shortened this acceptable validity period to 27 months, since the EV SSL Certificate Guidelines is unlikely to be updated to extend the period to 39 months.
