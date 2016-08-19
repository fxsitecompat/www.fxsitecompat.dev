---
title: "Non-standard Web Payments API has been removed"
date: "2016-03-28T14:28:00-05:00"
categories: ["misc"]
tags: []
versions: ["51"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1252570"
      title: "Bug 1252570 - Remove mozPay"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/FvzDoaPGQ3g/discussion"
      title: "Intent to unship: navigator.mozPay - mozilla.dev.platform"
---
The support for the non-standard [Web Payments API](https://wiki.mozilla.org/WebAPI/WebPayment), the [`navigator.mozPay`](https://developer.mozilla.org/en-US/docs/Web/API/Navigator/mozPay) method in particular, has been removed with Firefox 51. This API, drafted by Mozilla to enable [in-app payments](https://developer.mozilla.org/en-US/Marketplace/Monetization/In-app_payments_section/mozPay_iap) on Web applications, was initially implemented in Firefox OS and later enabled in Firefox for Android and the [Web App Runtime](https://developer.mozilla.org/en-US/Apps/Build/Architecture) of Firefox for desktop, but it has never been widely used. The Mozilla Marketplace is [removing the payment support](https://wiki.mozilla.org/Marketplace#Upcoming_Changes_to_Marketplace), while Firefox 47 has already [removed the Web App Runtime](https://www.fxsitecompat.com/en-CA/docs/2016/web-app-runtime-has-been-removed-from-firefox-for-desktop-and-android/) from desktop and Android.

In the future, Firefox may implement the standard Web Payments API which is being designed in the W3C [Web Payments Working Group](https://www.w3.org/Payments/WG/).
