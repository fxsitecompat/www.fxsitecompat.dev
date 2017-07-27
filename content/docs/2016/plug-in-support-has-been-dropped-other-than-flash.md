---
title: "Plug-in support has been dropped other than Flash"
date: "2016-10-04T00:57:00-07:00"
categories: ["plugins"]
tags: []
versions: ["52"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1269807"
      title: "Bug 1269807 - Remove support for all NPAPI plugins (except Flash)"
    - url: "https://blog.mozilla.org/futurereleases/2015/10/08/npapi-plugins-in-firefox/"
      title: "NPAPI Plugins in Firefox"
    - url: "https://groups.google.com/d/topic/mozilla.dev.tech.plugins/Cu1rOVEn45M/discussion"
      title: "Java plugin phase out timeline"
aliases:
    - "/en-CA/docs/2015/plug-in-support-will-be-dropped-by-the-end-of-2016-except-flash/"
---
For years, Mozilla has aimed to make the Web plug-in-free by enhancing Web standard technologies because plug-ins are negatively affecting the browser performance, security and user experience.

From [animation effects](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Animations/Using_CSS_animations), [video playback](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/Using_HTML5_audio_and_video), [drag & drop file upload](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/Drag_and_drop), [clipboard manipulation](https://hacks.mozilla.org/2015/09/flash-free-clipboard-for-the-web/) to [interactive 3D games](https://games.mozilla.org/), [realtime video chat](https://developer.mozilla.org/en-US/docs/Web/Guide/API/WebRTC), now everything can be done without a plug-in. Firefox offers a [build-in PDF reader](https://support.mozilla.org/en-US/kb/view-pdf-files-firefox-without-downloading-them) and [DRM support](https://support.mozilla.org/en-US/kb/enable-drm) as well.

Microsoft has [deprecated Silverlight](https://support.microsoft.com/en-us/lifecycle?C2=12905). Oracle has also announced the [deprecation of the Java browser plug-in](https://blogs.oracle.com/java-platform-group/entry/moving_to_a_plugin_free) in January 2016. As of April 2016, [QuickTime for Windows is no longer supported](https://support.apple.com/en-ca/HT201175) by Apple. The QuickTime plug-in for OS X has already been [disabled since 10.9 Mavericks](https://support.apple.com/en-ca/HT205081). Unity 5.4 shipped in July 2016 removed the support for the [Unity Web Player](https://blogs.unity3d.com/2015/10/08/unity-web-player-roadmap/) plug-in.

Therefore, the legacy [NPAPI plug-in](https://developer.mozilla.org/en-US/Add-ons/Plugins) support in Firefox, [deprecated since October 2015](https://blog.mozilla.org/futurereleases/2015/10/08/npapi-plugins-in-firefox/), has been removed from Firefox 52 with the exception of still-popular Adobe Flash Player. On the Windows 64-bit version of Firefox, [Flash and Silverlight are already the only supported plug-ins](https://www.fxsitecompat.com/en-CA/docs/2015/64-bit-firefox-for-windows-is-officially-available-flash-and-silverlight-are-the-only-supported-plug-ins/). Web publishers must develop a plan to replace any plug-in content, including Java applets and Silverlight videos, with alternative technologies.

For enterprise users who require Java in particular, Firefox 52 [Extended Support Release](https://www.mozilla.org/en-US/firefox/organizations/) (ESR) will keep the plug-in support enabled until May 2018.
