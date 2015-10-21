---
title: "Legacy Crypto API has been removed"
date: "2014-10-17T22:50:44-04:00"
categories: ["privacy-security"]
tags: []
versions: ["35"]
statuses: "affected"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1030963": "Bug 1030963 – remove proprietary window.crypto functions/properties"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1083118": "Bug 1083118 – window.crypto.signText replacement"
---
The Netscape-derived [legacy Crypto API](https://developer.mozilla.org/en-US/docs/JavaScript_crypto) implemented on [`window.crypto`](https://developer.mozilla.org/en-US/docs/Web/API/window.crypto) has been removed, including `enableSmartCardEvents` and `version` properties as well as `generateCRMFRequest`, `importUserCertificates`, `logout` and `signText` methods, in favor of the standard [Web Crypto API](https://developer.mozilla.org/en-US/docs/Web/API/SubtleCrypto). See the [MozillaWiki article](https://wiki.mozilla.org/SecurityEngineering/Removing_Proprietary_window.crypto_Functions) for details.

This legacy API has been [disabled with Firefox 33](https://www.fxsitecompat.com/en-US/docs/2014/legacy-crypto-api-has-been-disabled/) but enabled again with Firefox 34 because various banks and government agencies were still using it. Now the API has been completely removed but Firefox users who still need to use such sites can install the [signTextJS extension](https://addons.mozilla.org/en-US/firefox/addon/signtextjs/) alternatively.
