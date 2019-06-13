---
title: "Firefox 59 Developer Edition, project update, and 2 things you must do in 2018"
date: "2018-01-25T12:34:00-05:00"
---
Mozilla has shipped [Firefox 59 Beta and Developer Edition](https://www.mozilla.org/firefox/channel/desktop/) last week. Check out our [Firefox 59 compatibility notes](https://www.fxsitecompat.dev/en-CA/versions/59/) to get prepared for the final version coming this March. As with Firefox 58, more non-standard features are going away.

This is our first blog post in 2018 so we'd like to briefly summarize the things need to be done this year, by us and you.

## Our plan in 2018

First, we have a good news! Mozilla has become a *de facto* sponsor of this initiative. We are excited to have an opportunity to work more closely with people within the organization while our project manager [Kohei Yoshino](https://github.com/kyoshino) is serving the [Release Management team](https://release.mozilla.org/) as an independent contractor.

This small project is running since 2012 because we believe our documents, tweets and regression research will help improve the relationship between Mozilla and web developers as well as the product quality of Firefox. Now, Mozilla fuels the tireless effort. That's a win-win situation, obviously :-)

Actually we are still making plans for this year but prioritizing the overdue site redesign to serve you better.

## Your plan in 2018

### Move your site to HTTPS

Last week Mozilla announced their intent to [require HTTPS](https://blog.mozilla.org/security/2018/01/15/secure-contexts-everywhere/) for all new features plus some existing features. The use of the Geolocation API has already been limited to secure sites since [Firefox 55](https://www.fxsitecompat.dev/en-CA/docs/2017/use-of-geolocation-api-is-now-limited-to-secure-sites/). Application Cache and [WebVR](https://www.fxsitecompat.dev/en-CA/docs/2017/webvr-can-no-longer-be-used-on-insecure-sites/) are the next, potentially followed by the Notifications, Web Crypto and Encrypted Media Extensions APIs.

Even if you are not using any of these features, moving to HTTPS is no longer considered optional. [Let's encrypt](https://letsencrypt.org/) funded by Mozilla among others will offer [free wildcard certificates](https://letsencrypt.org/2017/07/06/wildcard-certificates-coming-jan-2018.html) starting from late February to make the transition even easier.

### Remove Flash dependency

Still relying on Flash by any chance? Sorry, but the [Flash plug-in support will be removed](https://blog.mozilla.org/futurereleases/2017/07/25/firefox-roadmap-flash-end-life/) from Firefox and other browsers by the end of 2020. Even at this time, more than one-third of Firefox users are not using Flash Player any more according to the latest [Firefox Hardware Report](https://hardware.metrics.mozilla.com/). You should be replacing any Flash content with standard technologies as soon as possible to ensure the maximum accessibility on your site.
