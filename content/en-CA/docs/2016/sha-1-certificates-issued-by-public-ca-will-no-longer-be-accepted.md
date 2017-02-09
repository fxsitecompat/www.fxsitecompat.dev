---
title: "SHA-1 certificates issued by public CA will no longer be accepted"
date: "2016-10-24T13:13:00-04:00"
categories: ["privacy-security"]
tags: []
versions: ["52"]
statuses: "affecting"
references:
    - url: "https://groups.google.com/d/topic/mozilla.dev.security.policy/wXvLQ26JyOA/discussion"
      title: "mozilla.dev.security.policy: Update to phasing out SHA-1 Certs"
    - url: "https://blog.mozilla.org/security/2015/10/20/continuing-to-phase-out-sha-1-certificates/"
      title: "Continuing to Phase Out SHA-1 Certificates"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1302140"
      title: "Bug 1302140 - add policy mode to completely disallow sha-1 signature except for certificates issued by non-built-in roots"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1321114"
      title: "Bug 1321114 - Remote SHA-1 shut-off"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1330043"
      title: "Bug 1330043 - disable sha1 in signatures on certificates issued by publicly-trusted roots"
    - url: "https://blog.mozilla.org/security/2016/10/18/phasing-out-sha-1-on-the-public-web/"
      title: "Phasing Out SHA-1 on the Public Web"
aliases:
    - "/docs/2015/sha-1-certificate-support-will-be-disabled-as-early-as-july-2016/"
---
The support for SSL certificates using the [weak SHA-1 hash algorithm](https://developer.mozilla.org/docs/Web/Security/Weak_Signature_Algorithm) has been [deprecated since Firefox 36](https://www.fxsitecompat.com/en-CA/docs/2014/sha-1-support-has-been-deprecated/). SHA-1 certificates issued after <time datetime="2016-01">January 2016</time> are [no longer accepted](https://www.fxsitecompat.com/en-CA/docs/2015/sha-1-based-certificates-with-validity-period-from-2016-will-not-be-validated/) since Firefox 48 except for manually-imported root certificates.

Firefox 53 coming <time datetime="2017-04">April 2017</time> removes the period condition so that any SHA-1 certificates issued by a public certificate authority will lead to the [Untrusted Connection](https://support.mozilla.org/en-US/kb/connection-untrusted-error-message) error. According to [Mozilla's announcement](https://blog.mozilla.org/security/2016/10/18/phasing-out-sha-1-on-the-public-web/), the current SHA-1 usage is less than 1%, and the support deprecation will be gradually expanded during the Firefox 51 Beta cycle while evaluating the impact.

If the [Web Console](https://developer.mozilla.org/en-US/docs/Tools/Web_Console) warns about a SHA-1 certificate when loading your site, contact the issuer immediately to replace it with a new SHA-2 certificate for free, regardless of the validity period.

**Update**: Fixed the affected version: not Firefox 51 but 53.

**Update 2**: Given that [Google Chrome 56](https://security.googleblog.com/2016/11/sha-1-certificates-in-chrome.html) has already removed the SHA-1 support in January 2017, Mozilla plans to [make this change earlier](https://mail.mozilla.org/pipermail/gofaster/2017-February/000563.html) with Firefox 52 shipping in March. We've updated this note's version again accordingly.
