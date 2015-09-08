---
title: "`<option>` cannot be selected in certain circumstances"
date: "2015-08-16T03:45:05-04:00"
categories: ["html"]
tags: ["regression"]
versions: "40"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1194733": "Bug 1194733 - [Not e10s] Version 40.0.2 has issue with jquery ibutton plugin"
---
The [`<option>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/option) element cannot be selected and the parent [`<select>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/select) element won't be closed, when [`Event.preventDefault`](https://developer.mozilla.org/en-US/docs/Web/API/Event/preventDefault) is called in a [`mouseup`](https://developer.mozilla.org/en-US/docs/Web/Events/mouseup) event handler on `<select>` or its ancestors. The [iButton jQuery plug-in](http://www.givainc.com/labs/ibutton_jquery_plugin.cfm) is known to be affected. Mozilla developers have identified the cause and are working on a solution.

**Update**: This issue has been fixed with Firefox 40.0.3 shipped on <time datetime="2015-08-27">August 27</time>.
