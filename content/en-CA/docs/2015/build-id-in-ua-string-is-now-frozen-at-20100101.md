---
title: "Build ID in UA string is now frozen at `20100101`"
date: "2015-10-27T01:35:00-07:00"
categories: ["dom", "networking", "privacy-security"]
tags: []
versions: ["25"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=728773"
      title: "Bug 728773 - Always freeze the build ID in the UA string at 20100101"
    - url: "https://developer.mozilla.org/en-US/docs/Web/HTTP/Gecko_user_agent_string_reference"
      title: "Gecko user agent string reference"
---
The Firefox build identifier, that can be retrieved via the HTTP `User-Agent` request header as well as the [`navigator.userAgent`](https://developer.mozilla.org/en-US/docs/Web/API/NavigatorID/userAgent) and [`navigator.productSub`](https://developer.mozilla.org/en-US/docs/Web/API/Navigator/productSub) DOM properties, has been frozen at `20100101` in order to reduce the browser's fingerprintability. While [`navigator.buildID`](https://developer.mozilla.org/en-US/docs/Web/API/Navigator/buildID) still returns the accurate build identifier, this property is considered to be [removed in the future](https://www.fxsitecompat.com/en-CA/docs/2015/navigator-buildid-will-be-removed/).
