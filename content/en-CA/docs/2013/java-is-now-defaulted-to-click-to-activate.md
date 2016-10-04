---
title: "Java is now defaulted to Click-to-Activate"
date: "2013-09-19T23:58:13-04:00"
categories: ["plugins"]
tags: []
versions: ["26"]
statuses: "affecting"
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=899080"
      title: "Bug 899080 – Make plugins default to click-to-play"
---
Starting with Firefox 26, [plug-ins](https://developer.mozilla.org/en-US/docs/Plugins) require user interaction to be activated. With the exception of the popular Adobe Flash Player, all plugin content embedded in a Web page is now disabled by default and enabled by a user's click. This change has been made in order to improve security and performance of the browser. See the [Mozilla Security Blog](https://blog.mozilla.org/security/2013/01/29/putting-users-in-control-of-plugins/) and the [Future Releases Blog](https://blog.mozilla.org/futurereleases/2013/09/24/plugin-activation-in-firefox/) for details. Web developers are encouraged to leverage modern Web technologies, including [HTML5](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/HTML5), to provide richer user experience. If that is not possible, see the [site author guide for click-to-activate plug-ins](https://developer.mozilla.org/en-US/docs/Site_Author_Guide_for_Click-To-Activate_Plugins).

**Update**: Mozilla has decided to [hold off turning on click-to-activate](https://bugzilla.mozilla.org/show_bug.cgi?id=941137) for all plug-ins except Java, on the Beta and Release channels, until a whitelisting strategy is defined.
