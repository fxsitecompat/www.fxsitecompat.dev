---
title: "`navigator.plugins` and `mimeTypes` are now unenumerable"
date: "2016-11-15T17:05:13-05:00"
categories: ["dom", "plugins"]
tags: []
versions: ["53"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=757726"
      title: "Bug 757726 - disallow enumeration of navigator.plugins"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=934107"
      title: "Bug 934107 - [meta] Remove use of plugin enumeration"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1270364"
      title: "Bug 1270364 - MimeTypeArray should have unenumerable named properties per spec"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1270366"
      title: "Bug 1270366 - PluginArray and Plugin should have unenumerable own properties per spec"
aliases:
    - "/en-CA/docs/2016/navigator-plugins-and-mimetypes-will-be-unenumerable/"
---
The [`navigator.plugins`](https://developer.mozilla.org/en-US/docs/Web/API/NavigatorPlugins/plugins) and [`navigator.mimeTypes`](https://developer.mozilla.org/en-US/docs/Web/API/NavigatorPlugins/mimeTypes) properties, returning a [`PluginArray`](https://developer.mozilla.org/en-US/docs/Web/API/PluginArray) and `MimeTypeArray` object respectively, have been made unenumerable with Firefox 53, following the [removal of the plug-in support other than Flash](https://www.fxsitecompat.com/en-CA/docs/2016/plug-in-support-has-been-dropped-other-than-flash/) in Firefox 52.

This change was originally planned for Firefox 28 to mitigate fingerprinting but cancelled due to considerable site compatibility issues.

These properties are actually still enumerable when using the [`Object.getOwnPropertyNames`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/getOwnPropertyNames) method or simply with the [spread syntax](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Spread_operator) like `[...navigator.plugins]`, however, it makes no more sense because only Flash Player will appear if installed.
