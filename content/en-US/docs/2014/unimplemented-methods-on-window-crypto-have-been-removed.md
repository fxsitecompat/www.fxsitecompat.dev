---
title: "Unimplemented methods on `window.crypto` have been removed"
date: "2014-04-03T19:31:02-04:00"
categories: ["dom"]
tags: []
versions: "31"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=897359": "Bug 897359 – Remove unimplemented method in nsCrypto"
---
The `disableRightClick`, [`popChallengeResponse`](https://developer.mozilla.org/en-US/docs/JavaScript_crypto/popChallengeResponse) and `random` methods have been removed from [`window.crypto`](https://developer.mozilla.org/en-US/docs/Web/API/window/crypto). Those were part of the non-standard [Crypto API](https://developer.mozilla.org/en-US/docs/JavaScript_crypto) of Netscape 4 but not implemented in [Gecko](https://developer.mozilla.org/en-US/docs/Mozilla/Gecko)-based Netscape 6 and Firefox, just throwing a `NS_ERROR_NOT_IMPLEMENTED` exception. Note that the standardized [`window.crypto.getRandomValues`](https://developer.mozilla.org/en-US/docs/Web/API/window/crypto/getRandomValues) method is available since [Firefox 21](https://developer.mozilla.org/en-US/Firefox/Releases/21) to get cryptographically random values.
