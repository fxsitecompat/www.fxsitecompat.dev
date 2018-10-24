---
title: "Firefox 63 shipping in October invalidates Symantec certificates used by many sites"
date: "2018-09-07T07:30:00-04:00"
---
Mozilla has shipped [Firefox 63 Beta and Developer Edition](https://www.mozilla.org/firefox/channel/desktop/). Check out our [Firefox 63 compatibility notes](https://www.fxsitecompat.com/en-CA/versions/63/) to get prepared for the final version coming late October.

The most important thing is, as you should be aware by now, the [distrust of Symantec certificates](https://www.fxsitecompat.com/en-CA/docs/2018/symantec-geotrust-rapidssl-thawte-verisign-certificates-will-all-be-distrusted-in-october-2018/) including ones issued under the GeoTrust, RapidSSL, Thawte and Verisign brands. This measure affects [various sites](https://bugzilla.mozilla.org/show_bug.cgi?id=1484006), so webmasters are highly encouraged to use [Firefox Nightly](https://www.mozilla.org/firefox/channel/desktop/#nightly) to double check if your site won't get a security error page.

By the way, this Saturday marks the 3rd anniversary of FxSiteCompat.com, and another milestone, 1,000 followers on [Twitter](https://twitter.com/FxSiteCompat), is also within reach. While scaling this kind of initiative is difficult, we have never wanted to remain as a mere documentation project. [Join us](https://www.fxsitecompat.com/en-CA/contribute/) if you're interested in outreach, analysis or [engineering](https://www.fxsitecompat.com/en-CA/tools/)!

**Update**: The distrust has been postponed until [Firefox 64 Beta](https://www.fxsitecompat.com/en-CA/blog/2018/firefox-64-beta-comes-with-symantec-distrust-enabled/).
