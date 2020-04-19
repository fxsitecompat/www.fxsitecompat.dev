---
title: "Firefox 64 Beta comes with Symantec distrust enabled"
date: "2018-10-24T15:00:00-04:00"
---
Mozilla has shipped [Firefox 64 Beta and Developer Edition](https://www.mozilla.org/firefox/channel/desktop/). Check out our [Firefox 64 compatibility notes](https://www.fxsitecompat.dev/en-CA/releases/64/) to get prepared for the final version coming December.

The [distrust of Symantec, GeoTrust, RapidSSL, Thawte and Verisign certificates](https://www.fxsitecompat.dev/en-CA/docs/2018/symantec-geotrust-rapidssl-thawte-verisign-certificates-will-all-be-distrusted-in-october-2018/) is now enabled in the latest Beta and Developer Edition after being postponed from Firefox 63. According to Mozilla's [TLS Canary](http://tlscanary-plot-8e95d89854d73f4d.elb.us-west-2.amazonaws.com/), 1% of the top 1,000 sites and 4% of the top 100 sites are still using an affected certificate as of this writing. Given the statistics, webmasters are highly encouraged to double check their site using one of the pre-release builds.

Other changes in Firefox 64 are mainly removals of non-standard features. The [unprefixed Fullscreen API](https://www.fxsitecompat.dev/en-CA/docs/2018/fullscreen-api-has-been-unprefixed/) may also draw attention from web developers.
