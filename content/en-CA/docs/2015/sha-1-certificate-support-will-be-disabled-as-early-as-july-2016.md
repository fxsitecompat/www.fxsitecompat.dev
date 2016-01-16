---
title: "SHA-1 certificate support will be disabled as early as July 2016"
date: "2015-10-25T13:37:00-07:00"
categories: ["privacy-security"]
tags: []
versions: ["future"]
statuses: "affected"
references:
    "https://groups.google.com/d/topic/mozilla.dev.security.policy/wXvLQ26JyOA/discussion": "mozilla.dev.security.policy: Update to phasing out SHA-1 Certs"
    "https://blog.mozilla.org/security/2015/10/20/continuing-to-phase-out-sha-1-certificates/": "Continuing to Phase Out SHA-1 Certificates"
---
The support for SSL certificates using the [weak SHA-1 hash algorithm](https://developer.mozilla.org/docs/Web/Security/Weak_Signature_Algorithm) has been [deprecated since Firefox 36](https://www.fxsitecompat.com/en-CA/docs/2014/sha-1-support-has-been-deprecated/). SHA-1 certificates issued after <time datetime="2016-01">January 2016</time> are [no longer accepted](https://www.fxsitecompat.com/en-CA/docs/2015/sha-1-based-certificates-with-validity-period-from-2016-will-not-be-validated/), leading to the [Untrusted Connection](https://support.mozilla.org/en-US/kb/connection-untrusted-error-message) error.

All SHA-1 certificates will be rejected after <time datetime="2017-01">January 2017</time> according to Mozilla's deprecation plan, but this date may be pushed forward to <time datetime="2016-07">July 2016</time> in the light of recent attacks on SHA-1. We will update this document based on the latest timeline.

[More than a quarter of sites](http://news.netcraft.com/archives/2015/10/19/one-million-ssl-certificates-still-using-insecure-sha-1-algorithm.html) are still using a SHA-1 certificate. If the [Web Console](https://developer.mozilla.org/en-US/docs/Tools/Web_Console) warns about a SHA-1 certificate when loading your site, contact the issuer immediately to replace it with a new SHA-2 certificate for free, regardless of the validity period.
