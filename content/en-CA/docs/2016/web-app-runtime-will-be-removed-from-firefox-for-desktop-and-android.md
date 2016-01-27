---
title: "Web App Runtime will be removed from Firefox for desktop and Android"
date: "2016-01-14T22:08:00-05:00"
categories: ["misc"]
tags: []
versions: ["future"]
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1235869": "Bug 1235869 - Remove support for WebRT"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1238079": "Bug 1238079 - disable and remove runtime"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1238576": "Bug 1238576 - Stop exposing navigator.mozApps on desktop and Android"
    "https://groups.google.com/d/topic/firefox-dev/WV2XkVN3sWQ/discussion": "firefox-dev: disabling the desktop/Android Web Runtimes"
    "https://groups.google.com/d/topic/mozilla.dev.webapps/PUm4nx4A3X8/discussion": "mozilla.dev.webapps: alternatives to desktop/Android web runtimes"
---
The non-standard [Open Web Apps JavaScript API](https://developer.mozilla.org/en-US/Apps/Build/JavaScript_API) and [Web App Runtime](https://developer.mozilla.org/en-US/Apps/Build/Architecture), that allowed Web applications to be installed and run on the user's device like native applications, will be removed from Firefox for [desktop](https://developer.mozilla.org/en-US/Marketplace/Options/Open_web_apps_for_desktop) and [Android](https://developer.mozilla.org/en-US/Marketplace/Options/Open_web_apps_for_android) in the future.

Those functionalities were invented by Mozilla Labs in 2011 then became an integral part of [Firefox OS](https://developer.mozilla.org/en-US/Apps/Build/Building_apps_for_Firefox_OS) built on modern Web technologies. However, the runtime has not been widely used and actively developed on other platforms.

The [Firefox Marketplace](https://developer.mozilla.org/en-US/Marketplace) will stop distributing apps to desktop computers and Android devices accordingly. Firefox OS is not affected at this moment. Open Web Apps are not supported on WebKit-based Firefox for iOS.
