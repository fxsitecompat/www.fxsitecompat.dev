---
title: "Firefox 60 Developer Edition, one step toward a safer web, and JavaScript library compatibility"
date: "2018-03-19T20:13:00-04:00"
---
Mozilla has shipped [Firefox 60 Beta and Developer Edition](https://www.mozilla.org/firefox/channel/desktop/). Check out our [Firefox 60 compatibility notes](https://www.fxsitecompat.dev/en-CA/versions/60/) to get prepared for the final version coming early May.

As you'll see, there are several security-related changes including secure context requirements along with the [first round of the Symantec certificate distrust actions](https://www.fxsitecompat.dev/en-CA/docs/2018/symantec-certificates-issued-before-june-2016-are-now-distrusted/). If you have a SSL/TLS server certificate with the GeoTrust, RapidSSL, Symantec, Thawte or Verisign brand, take an immediate action to avoid Insecure Connection error pages on your site. Don't have any certificate yet? Get yours from [Let's Encrypt](https://letsencrypt.org/) today, for free.

`Array.prototype.values()` being [re-enabled with Firefox 60](https://www.fxsitecompat.dev/en-CA/docs/2018/array-prototype-values-is-now-enabled-again/) was an example of how adding a new feature could [break existing web apps](https://www.fxsitecompat.dev/en-CA/docs/2016/array-prototype-values-breaks-some-legacy-apps/), and it's not new or the last —
`Array.prototype.find()` [added with Firefox 25](https://www.fxsitecompat.dev/en-CA/docs/2013/es6-array-methods-have-been-added/) broke sites using the Sugar library, while `Array.prototype.flatten()` being implemented is known to [affect MooTools](https://bugzilla.mozilla.org/show_bug.cgi?id=1443630) which actually had the [same issue](https://www.fxsitecompat.dev/en-CA/docs/2012/mootools-1-2-x-is-not-compatible-with-firefox-18-and-newer/) with `String.prototype.contains()`. Be sure to keep your JavaScript library updated!
