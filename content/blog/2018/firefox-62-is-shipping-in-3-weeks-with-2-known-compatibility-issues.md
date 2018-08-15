---
title: "Firefox 62 is shipping in 3 weeks with 2 known compatibility issues"
date: "2018-08-15T15:09:00-04:00"
---
Sorry for the late blog post for the upcoming release since we have been busy with other stuff for a while!

Firefox 62 has been on the Beta/DevEdition channel now for 8 weeks, and will be shipping in 3 weeks on September 5. You may already have read through our [Firefox 62 site compatibility notes](https://www.fxsitecompat.com/en-CA/versions/62/), but here are some updates:

* [`URL.createObjectURL()` no longer accepts `MediaStream` as argument](https://www.fxsitecompat.com/en-CA/docs/2018/url-createobjecturl-no-longer-accepts-mediastream-as-argument/): This change is known to break *Facebook Live*. If you have a similar live streaming service, make sure it continues working properly.
* [Support for `Event.prototype.srcElement` has been added](https://www.fxsitecompat.com/en-CA/docs/2018/support-for-event-prototype-srcelement-has-been-added/): The IE-derived property has been implemented for web compatibility, and it breaks Chinese portal site *QQ.com*. Firefox 63 has [another addition](https://www.fxsitecompat.com/en-CA/docs/2018/window-event-has-been-added-for-compatibility-but-some-browser-detections-are-broken/) you should be aware of.
* [`getComputedStyle()` no longer returns `null` when style can't be retrieved](https://www.fxsitecompat.com/en-CA/docs/2018/getcomputedstyle-no-longer-returns-null-when-style-can-t-be-retrieved/): This note was posted yesterday. Please check it out if you haven't.

We also have started preparing [Firefox 63 site compatibility notes](https://www.fxsitecompat.com/en-CA/versions/63/). One notable change is the [distrust of Symantec, GeoTrust, RapidSSL, Thawte, Verisign certificates](https://www.fxsitecompat.com/en-CA/docs/2018/symantec-geotrust-rapidssl-thawte-verisign-certificates-will-all-be-distrusted-in-october-2018/) which is already known to affect some major sites as well, including *PayPal* and *Etsy*. You should double check your site's SSL/TLS certificate to avoid any unexpected service interruption.
