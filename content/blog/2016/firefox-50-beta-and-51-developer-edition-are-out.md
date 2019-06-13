---
title: "Firefox 50 Beta and 51 Developer Edition are out!"
date: "2016-09-24T19:33:00-04:00"
---
Mozilla has shipped Firefox 49, [Firefox 50 Beta and 51 Developer Edition](https://www.mozilla.org/firefox/channel/) this week. Check out our [site compatibility documents](https://www.fxsitecompat.dev/en-CA/docs/) for each version:

* [Firefox 49 Site Compatibility](https://www.fxsitecompat.dev/en-CA/versions/49/)
* [Firefox 50 Site Compatibility](https://www.fxsitecompat.dev/en-CA/versions/50/)
* [Firefox 51 Site Compatibility](https://www.fxsitecompat.dev/en-CA/versions/51/)

One notable change in Firefox 49 is the [`#RGBA` colour value support](https://www.fxsitecompat.dev/en-CA/docs/2016/support-for-rgba-colour-values-may-validate-previously-invalid-values/), which is affecting a Microsoft application and probably others. You may want to scan your stylesheets to prevent text being displayed as transparent.

Firefox 50 Beta enables the [insecure login form warning](https://www.fxsitecompat.dev/en-CA/docs/2015/non-https-sites-containing-login-form-will-be-marked-insecure/) that can still be seen on various sites. It's time to encrypt your entire site to protect visitors.

Don't forget that Firefox 52, currently on the Nightly channel, will finally [drop the plug-in support except Flash](https://www.fxsitecompat.dev/en-CA/docs/2015/plug-in-support-will-be-dropped-by-the-end-of-2016-except-flash/). If your site has any content relying on a plug-in such as Silverlight or Java, you should have a plan to replace it as soon as possible.
