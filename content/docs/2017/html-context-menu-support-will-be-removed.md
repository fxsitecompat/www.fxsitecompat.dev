---
title: "HTML context menu support will be removed"
date: "2017-07-17T14:06:00-04:00"
categories: ["html"]
tags: []
versions: ["future"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1372276"
      title: "Bug 1372276 - Remove HTML context menu (<menu> and <menuitem> tag) support"
---
The support for [HTML5 context menus](https://hacks.mozilla.org/2011/11/html5-context-menus-in-firefox-screencast-and-code/), introduced with Firefox 8, will be removed soon. Other browser vendors were not interested in the feature, and therefore it has already been removed from the HTML spec, leaving Firefox as the only browser implementing the [`<menu>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/menu) and [`<menuitem>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/menuitem) elements as well as the [`contextmenu`](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/contextmenu) global attribute.

If desired, you can instead create your own context menu as seen in some rich web applications like *Google Drive*. The [WAI-ARIA](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA) standard provides a way to [create accessible menus](https://www.w3.org/WAI/GL/wiki/Using_ARIA_menus) which is highly recommended.
