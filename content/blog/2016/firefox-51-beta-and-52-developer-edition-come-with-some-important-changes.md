---
title: "Firefox 51 Beta and 52 Developer Edition come with some important changes"
date: "2016-12-04T15:30:00-05:00"
---
Mozilla has shipped [Firefox 51 Beta and 52 Developer Edition](https://www.mozilla.org/firefox/channel/desktop/) on November 16 and 21 respectively. Sorry we haven't posted this earlier! Due to the Mozilla All Hands happening this week (our project manager [Kohei](https://mozillians.org/u/kohei.yoshino/) will be there as a volunteer) and upcoming holiday season, [Firefox 51 won't hit the streets until late January](https://release.mozilla.org/firefox/50/2016/11/22/Firefox50-planned-dot-release.html). Anyway, take a look at our site compatibility documents for each version:

* [Firefox 51 Site Compatibility](https://www.fxsitecompat.com/en-CA/versions/51/)
* [Firefox 52 Site Compatibility](https://www.fxsitecompat.com/en-CA/versions/52/)

Here are some highlights:

* As of Firefox 51, [SHA-1 certificates issued by public CA will no longer be accepted](https://www.fxsitecompat.com/en-CA/docs/2016/sha-1-certificates-issued-by-public-ca-will-no-longer-be-accepted/). According to Mozilla, the current SHA-1 usage is less than 1% but not zero, so it's a good idea to use the Developer Edition to double check if your secure site is not blocked.
* Firefox 51 also [enables the insecure password input warning by default](https://www.fxsitecompat.com/en-CA/docs/2016/insecure-password-input-warning-will-be-enabled-by-default/). This breaks nothing in terms of compatibility, but you probably don't want your customers to see a broken padlock icon. Let's put your login form on an HTTPS page today.
* Firefox 52 will [enable touch event support on Windows desktop](https://www.fxsitecompat.com/en-CA/docs/2016/touch-event-support-has-been-re-enabled-on-windows-desktop/). As explained in the document, you should never rely on touch events to detect mobile, or your site will be unusable for people using a touchscreen laptop.
* Last but certainly not least, Firefox 52 finally [removes the support for plug-ins other than Flash](https://www.fxsitecompat.com/en-CA/docs/2016/plug-in-support-has-been-dropped-other-than-flash/). This means Java applets or Silverlight videos will no longer work. If you are affected, take a quick action before Firefox 52 goes public in early March.

Now as 2016 is almost over, we are going to have a plan for 2017 to upgrade the project. More tweets? An enhanced website? Let us know what you need. And, given it's a year-end fundraising season, we are more than happy to see your [small donation](https://www.fxsitecompat.com/en-CA/contribute/#donate-to-us)! It's obviously not tax-deductible, but even a few dollars will make a difference. Thank you for your support!
