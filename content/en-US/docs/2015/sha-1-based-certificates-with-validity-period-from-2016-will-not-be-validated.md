---
title: "SHA-1-based certificates with validity period from 2016 will not be validated"
date: "2015-09-13T21:46:00-04:00"
categories: ["privacy-security"]
tags: []
versions: "43"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=942515": "Bug 942515 - Show Untrusted Connection Error for SHA-1-based SSL certificates with notBefore >= 2016-01-01"
    "https://blog.mozilla.org/security/2014/09/23/phasing-out-certificates-with-sha-1-based-signature-algorithms/": "Phasing Out Certificates with SHA-1 based Signature Algorithms"
---
The support for certificates using the [weak SHA-1 hash algorithm](https://developer.mozilla.org/docs/Web/Security/Weak_Signature_Algorithm) has been [deprecated since Firefox 36](https://www.fxsitecompat.com/en-US/docs/2014/sha-1-support-has-been-deprecated/). As a part of the deprecation process, SHA-1-based certificates with a period of validity beginning on or after <time datetime="2016-01-01">January 1, 2016</time> are no longer validated by Firefox 43 and later, and "[This Connection is Untrusted](https://support.mozilla.org/kb/connection-untrusted-error-message)" alert page will be displayed on sites using such a certificate.

Webmasters: Open the [Web Console](https://developer.mozilla.org/docs/Tools/Web_Console), load your site, and make sure a SHA-1-based certificate is *not* used. If the Console warns about a SHA-1-based certificate, contact the issuer to replace it with a new SHA-2-based one for free, regardless of the validity period. Firefox, among other browsers, will show the Untrusted Connection error message for all SHA-1-based certificates after <time datetime="2017-01">January 2017</time>.
