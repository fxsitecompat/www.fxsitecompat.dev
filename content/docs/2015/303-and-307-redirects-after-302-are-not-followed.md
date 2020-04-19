---
title: "303 and 307 redirects after 302 are not followed"
date: "2015-10-20T21:42:00-07:00"
categories: ["networking"]
tags: [""]
releases: ["39"]
statuses: "regressed"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1196882"
      title: "Bug 1196882 - Firefox not following 303/7 Status Code after 302"
---
Firefox 39 has tightened the handling of non-compliant HTTP responses so the browser no longer follows a redirect with the 303 See Other or 307 Temporary Redirect status code following after 302 Found. However, this new behaviour has been reverted with Firefox 41 due to Web compatibility issues.
