---
title: "Local files are now each given a different origin"
date: "2019-07-15T12:29:00-04:00"
categories: ["privacy-security"]
tags: []
versions: ["68", "68-esr"]
statuses: "affecting"
references:
    - url: "https://www.mozilla.org/en-US/security/advisories/mfsa2019-21/#CVE-2019-11730"
      title: "CVE-2019-11730: Same-origin policy treats all files in a directory as having the same-origin"
---
Firefox 68 has tightened the [same-origin policy](https://developer.mozilla.org/docs/Web/Security/Same-origin_policy) to prevent locally-saved malicious HTML content from accessing other files in the same directory. This could be an issue if you're testing your site on your own machine directly through the `file://` URL, and having a script in a separate file or embedding an `<iframe>`, for example.

While a simple, self-contained HTML file may still work, it's highly recommended to set up a local server if you want to test a site with assets. There are easy-to-use tools like [MAMP](https://www.mamp.info/) or [XAMPP](https://www.apachefriends.org/), and [macOS](https://discussions.apple.com/docs/DOC-3083) also comes with the Apache server.

**Update**: This change is affecting various other things as well, including web fonts, workers and XSLT. [Bug 1566172](https://bugzilla.mozilla.org/show_bug.cgi?id=1566172) has a list of those cases.
