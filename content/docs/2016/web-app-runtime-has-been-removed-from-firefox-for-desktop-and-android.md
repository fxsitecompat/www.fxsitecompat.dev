---
title: "Web App Runtime has been removed from Firefox for desktop and Android"
date: "2016-02-09T08:19:00-05:00"
categories: ["misc"]
tags: []
releases: ["47", "52-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1235869"
      title: "Bug 1235869 - Remove support for WebRT"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1238079"
      title: "Bug 1238079 - disable and remove runtime"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1238576"
      title: "Bug 1238576 - Stop exposing navigator.mozApps on desktop and Android"
    - url: "https://groups.google.com/d/topic/firefox-dev/WV2XkVN3sWQ/discussion"
      title: "firefox-dev: disabling the desktop/Android Web Runtimes"
    - url: "https://groups.google.com/d/topic/mozilla.dev.webapps/PUm4nx4A3X8/discussion"
      title: "mozilla.dev.webapps: alternatives to desktop/Android web runtimes"
aliases:
    - "/en-CA/docs/2016/web-app-runtime-will-be-removed-from-firefox-for-desktop-and-android/"
---
The non-standard [Open Web Apps JavaScript API](https://developer.mozilla.org/Apps/Build/JavaScript_API) and [Web App Runtime](https://developer.mozilla.org/Apps/Build/Architecture), that allowed Web applications to be installed and run on the user's device like native applications, have been removed from Firefox 47 for [desktop](https://developer.mozilla.org/Marketplace/Options/Open_web_apps_for_desktop) and [Android](https://developer.mozilla.org/Marketplace/Options/Open_web_apps_for_android).

Those functionalities were invented by Mozilla Labs in 2011 then became an integral part of [Firefox OS](https://developer.mozilla.org/Apps/Build/Building_apps_for_Firefox_OS) built on modern Web technologies. However, the runtime has not been widely used and actively developed on other platforms.

The [Firefox Marketplace](https://developer.mozilla.org/Marketplace) will stop distributing apps to desktop computers and Android devices accordingly. Firefox OS is not affected at this moment. Open Web Apps are not supported on WebKit-based Firefox for iOS.
