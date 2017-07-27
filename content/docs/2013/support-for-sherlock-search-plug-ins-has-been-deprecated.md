---
title: "Support for Sherlock search plug-ins has been deprecated"
date: "2013-05-19T07:35:00-04:00"
categories: ["misc"]
tags: []
versions: ["24"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=862143"
      title: "Bug 877135 – stop loading Sherlock files from disk"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=862137"
      title: "Bug 862137 – stop supporting Sherlock search engines"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=862148"
      title: "Bug 862148 – stop supporting installation of Sherlock plugins from the web"
---
Starting with Firefox 24, Sherlock-format search engine plug-ins are no longer loaded from local files. Sherlock support and the `window.sidebar.addSearchEngine` function, which allows Web pages to install Sherlock plug-ins, will also be removed in the near future, along with the removal of the non-standard [`window.sidebar`](https://developer.mozilla.org/en-US/docs/Web/API/window.sidebar) API. Web publishers should [provide OpenSearch plug-ins](https://developer.mozilla.org/en-US/docs/Creating_OpenSearch_plugins_for_Firefox) instead.

**Update**: The Sherlock support has been [removed with Firefox 44](https://www.fxsitecompat.com/en-CA/docs/2015/sherlock-search-plug-ins-are-no-longer-supported/).
