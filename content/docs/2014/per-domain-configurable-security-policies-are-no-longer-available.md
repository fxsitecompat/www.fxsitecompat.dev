---
title: "Per-domain Configurable Security Policies are no longer available"
date: "2014-02-07T11:57:09-05:00"
categories: ["privacy-security"]
tags: []
versions: ["29"]
statuses: "affecting"
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=913734"
      title: "Bug 913734 – Remove domain policy goop from CAPS"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=995943"
      title: "Bug 995943 – local (file://) links don\'t work even when configured for company\'s internal system"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1004260"
      title: "Bug 1004260 – Firefox 29 broke clipboard access; restore the CAPS allowclipboard policy until the Clipboard API allows click-to-copy"
---
[Configurable Security Policies](http://kb.mozillazine.org/Security_Policies) (CAPS) of Firefox allows users to customize their browser's advanced security settings and have different policies for different sites. Though CAPS has no user interface, advanced or enterprise users can add some hidden preferences to control various capabilities. The per-domain policy of CAPS has been removed from Firefox 29 except the script blocking (the [NoScript](https://addons.mozilla.org/en-US/firefox/addon/noscript/) extension offers the UI).

In order to respond to demands of enterprise users, the [`localfilelinks` policy](http://kb.mozillazine.org/Links_to_local_pages_do_not_work) has been restored with Firefox 30. This allows users to follow links on a Web page (`http://` or `https://`) to the local file system (`file:///`) especially on corporate internal applications. For the meantime, [Firefox Beta](https://www.mozilla.org/firefox/channel/) or the [caps-fileuri](https://addons.mozilla.org/en-US/firefox/addon/caps-fileuri/) extension created by a Mozilla developer can be used to workaround this restriction.

The removal of [`allowclipboard` policy](http://kb.mozillazine.org/Granting_JavaScript_access_to_the_clipboard) support broke the copy/paste buttons on some rich text editors like *CKEditor*. The standard [Clipboard API](https://developer.mozilla.org/docs/Web/API/ClipboardEvent)'s click-to-copy support will be implemented in the near future. The general keyboard shortcuts, <kbd>Ctrl</kbd>+<kbd>C</kbd> and <kbd>Ctrl</kbd>+<kbd>V</kbd>, should always work.

**Update**: The click-to-copy support has been [implemented with Firefox 41](https://www.fxsitecompat.com/en-CA/docs/2015/document-execcommand-for-cut-copy-and-paste-no-longer-throws/).
