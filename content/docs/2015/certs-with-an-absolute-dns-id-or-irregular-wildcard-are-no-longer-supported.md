---
title: "Certs with an absolute DNS ID or irregular wildcard are no longer supported"
date: "2015-01-16T09:37:54-05:00"
categories: ["privacy-security"]
tags: []
versions: ["37"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1107790"
      title: "Bug 1107790 – Remove support for absolute hostnames in presented DNS IDs and name constraints"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1107791"
      title: "Bug 1107791 – Limit wildcard DNS ID support to names of the form *.example.com (not foo*.example.com)"
---
Certificates using the absolute presented DNS ID syntax that ends with a trailing dot like `example.com.` are no longer considered valid. Also, the wildcard DNS ID support has been limited to the `*.example.com` form, therefore other forms like `foo*.example.com` or `*foo.example.com` are no longer supported.
