---
title: "Legacy Crypto API has been disabled"
date: "2014-07-22T05:06:26-04:00"
categories: ["privacy-security"]
tags: []
versions: ["33"]
statuses: "reverted"
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1036546"
      title: "Bug 1036546 – soft-disable proprietary window.crypto functions/properties before removing them entirely "
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1083118"
      title: "Bug 1083118 – window.crypto.signText replacement"
---
The Netscape-derived [legacy Crypto API](https://developer.mozilla.org/en-US/docs/JavaScript_crypto) implemented on [`window.crypto`](https://developer.mozilla.org/en-US/docs/Web/API/window.crypto) has been disabled, including `enableSmartCardEvents` and `version` properties as well as `generateCRMFRequest`, `importUserCertificates`, `logout` and `signText` methods. These features have never been standardized and therefore will be removed with Firefox 34, while the standard [Web Crypto API has been actively implemented](https://bugzilla.mozilla.org/show_bug.cgi?id=865789). See the [MozillaWiki article](https://wiki.mozilla.org/SecurityEngineering/Removing_Proprietary_window.crypto_Functions) for details.

**Update**: Feedbacks on Firefox 33 have revealed that various banks and government agencies are still using this legacy Crypto API, the `crypto.signText` method in particular. Therefore, Mozilla has decided to bring the API back with Firefox 34 and remove it again in the near future once a substitute Firefox extension is developed. Firefox 33 users can still re-enable the API by setting the `dom.unsafe_legacy_crypto.enabled` pref to `true`, and Firefox 31 ESR users are not affected by this change.

**Update**: The legacy Crypto API has been [removed with Firefox 35](https://www.fxsitecompat.com/en-CA/docs/2014/legacy-crypto-api-has-been-removed/).
