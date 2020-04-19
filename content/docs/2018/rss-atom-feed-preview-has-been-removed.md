---
title: "RSS/Atom feed preview has been removed"
date: "2018-10-23T01:07:00-04:00"
categories: ["misc"]
tags: []
versions: ["64", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1477667"
      title: "Bug 1477667 - [meta] Remove feed reader and live bookmarks support from Firefox"
---
Firefox 64 has removed the RSS/Atom feed preview and built-in [Live Bookmarks](https://support.mozilla.org/kb/live-bookmarks) feed reader functionality because of the low adoption rate. From now on, web feeds will be displayed or downloaded as regular XML files, depending on the server's configuration.

For a better user experience, webmasters may want to replace direct feed links with subscription links of external services such as [Feedly](https://feedly.com/factory.html), or at least make sure that feeds are not downloaded. For your reference, the proper MIME types of RSS and Atom feeds are `application/rss+xml` and `application/atom+xml` respectively.

Common feed readers may discover feeds with `<link rel="alternate">` so you should keep it.
