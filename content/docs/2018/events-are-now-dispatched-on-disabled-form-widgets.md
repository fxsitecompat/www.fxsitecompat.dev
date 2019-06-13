---
title: "Events are now dispatched on disabled form widgets"
date: "2018-12-20T23:22:00-05:00"
categories: ["dom"]
tags: []
versions: ["65"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=329509"
      title: "Bug 329509 - Do not prevent event dispatching even if there is no prescontext or (form) element is disabled"
---
Starting with Firefox 65, form elements like `<input>`, `<textarea>`, `<button>` and `<select>` will allow to dispatch standard and custom events even when they are disabled. This change aims at improving the interoperability among browsers and responding to web developer needs.

Given that the element is disabled and unfocusable, most of events such as `mousedown`, `mouseup`, `click`, `focus` and `input` won't be fired by regular user interactions, but `mouseover`, `mouseenter`, `mousemove`, `mouseout` and `mouseleave` will now be fired unlike the current version of Google Chrome, Apple Safari and Microsoft Edge.

In order to avoid any unexpected behaviour, it might be better to always check the `disabled` property on the form element before further processing within your event handler.

**Update**: CSS animation and transition events will also be fired on disabled elements on [Firefox 67](https://www.fxsitecompat.dev/en-CA/docs/2019/css-animation-and-transition-events-are-now-fired-on-disabled-form-widgets/) and later.
