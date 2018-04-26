---
title: "Flash is forced windowless mode on Firefox for 64-bit Windows, affecting Stage 3D"
date: "2016-06-10T20:23:00-04:00"
categories: ["plugins"]
tags: []
versions: ["47"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1271398"
      title: "Bug 1271398 - [Regression] Problems with Adobe Flash Player Stage3D and Firefox x64 >=v47"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/EwI9Fq4DPy4/discussion"
      title: "Flash on Firefox Win64 runs on windowless mode only"
---
On Firefox 47 and later, the Adobe Flash Player plug-in runs only in the windowless mode on the 64-bit version of Firefox for Windows. [`wmode=direct`](https://helpx.adobe.com/flash/kb/flash-object-embed-tag-attributes.html#main_Using_Window_Mode__wmode__values_) is ignored and `wmode=opaque` will be used instead. This change was required to solve several sandbox compatibility issues including input method editors (IMEs) and file picker dialog.

However, some interactive Flash content is broken due to the [Stage 3D](https://www.adobe.com/devnet/flashplayer/stage3d.html) APIs not working in the windowless mode. *Forge of Empires*, a popular online game, is known to be affected. Since the 64-bit version of Firefox is not yet distributed widely, the number of affected users is limited at this time. Game developers can ask Firefox users to use the 32-bit version for the meanwhile.

According to a bug comment, there is a plan to re-enable `wmode=direct` for Flash Player Beta that supports a new accelerated drawing model handled in the windowless mode.

**Update**: Mozilla has no intention to revert the change, because the 64-bit version is not a default Firefox download option, and a strong sandbox and proper IME handling are considered more important than the Stage 3D support. Anyhow, developers are encouraged to migrate from Flash to WebGL as soon as possible. Visit [games.mozilla.org](https://games.mozilla.org/) for further information.

**Update**: Flash Player 23, currently in Beta, should work with the Windows 64-bit version of Firefox 49 and later.
