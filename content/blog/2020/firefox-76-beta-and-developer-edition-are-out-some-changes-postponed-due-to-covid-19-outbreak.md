---
title: "Firefox 76 Beta and Developer Edition are out, some changes postponed due to COVID-19 outbreak"
date: "2020-04-07T22:28:00-04:00"
---
Mozilla has shipped [Firefox 76 Beta and Developer Edition](https://www.mozilla.org/firefox/channel/desktop/) today with [only a few changes related to site compatibility](https://www.fxsitecompat.dev/en-CA/versions/76/).

As you may already know, the current COVID-19 pandemic is more or less affecting the development of Firefox along with other browsers. During this unusual time, a huge number of people around the world are working and studying at home, using a desktop browser [including Firefox](https://blog.mozilla.org/data/2020/03/30/opening-data-to-understand-social-distancing/), and relying on various online resources.

While Mozilla maintains the [rapid release schedule](https://wiki.mozilla.org/Release_Management/Calendar), the organization has postponed several backward incompatible changes to mitigate the risk of breakage:

* [Removing TLS 1.0/1.1 support](https://www.fxsitecompat.dev/en-CA/docs/2020/tls-1-0-1-1-support-has-been-removed/)
* [Removing DTLS 1.0 support from WebRTC](https://www.fxsitecompat.dev/en-CA/docs/2020/dtls-1-0-support-in-webrtc-has-been-removed/)
* Removing FTP support (coming soon to Firefox Nightly)
* [Enforcing MIME check for worker scripts](https://www.fxsitecompat.dev/en-CA/docs/2020/worker-scripts-with-wrong-mime-type-will-be-blocked-from-loading-with-worker-or-sharedworker/)
* [Rotating JPEG images](https://www.fxsitecompat.dev/en-CA/docs/2020/jpeg-images-are-now-rotated-by-default-according-to-exif-data/)

These changes will be made later this year once the situation is improved. We’ll keep you posted.
