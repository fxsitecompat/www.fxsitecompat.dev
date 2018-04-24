---
title: "Non-printable keys will soon stop firing `keypress` event"
date: "2018-03-03T04:49:00-05:00"
categories: ["dom"]
tags: []
versions: ["61"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1440189"
      title: "Bug 1440189 - Stop dispatching keypress event on web content in Nightly"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1442528"
      title: "Bug 1442528 - Keyboard handling in Google Docs is broken if \"dom.keyboardevent.keypress.dispatch_non_printable_keys_only_system_group_in_content\" is true"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1454833"
      title: "Bug 1454833 - Keyboard shortcuts do not work on hangouts.google.com in strict keypress event dipatching mode"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1455059"
      title: "Bug 1455059 - Tab no longer works in Etherpad"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1455229"
      title: "Bug 1455229 - Add Google Keep into the blacklist to use legacy keypress event behavior"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1456038"
      title: "Bug 1456038 - Google Inbox Keyboard Shortcuts Broken"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/wW9el-i5mtA/discussion"
      title: "Intent to stop dispatching \"keypress\" event for non-printable keys and key combinations in Nightly and early Beta"
---
In order to follow the [UI Events spec](https://w3c.github.io/uievents/) and other browsers' behaviour, Firefox will stop dispatching the `keypress` event for non-printable keys and key combinations in the near future.

[Non-printable keys](https://developer.mozilla.org/en-US/docs/Web/API/KeyboardEvent/keyCode#Non-printable_keys_(function_keys)) are function keys like Home, End, Tab, Escape, Backspace, Page Down, arrows, etc. Non-printable key combinations include Ctrl+A, Alt+G, Command+Shift+M and so on. Web developers should be using the `keydown` event instead to handle those keys.

An exception is the Enter key; pressing Enter with no modifiers, Shift+Enter or Ctrl+Enter will fire the `keypress` event as before, which is invalid in the current spec but compatible with other browsers.

This change has been made to the Nightly and early Beta/DevEdition channels as of Firefox 60. Other channels will also adopt the standard-compliant behaviour once compatibility issues on major sites are solved. Currently, some keyboard shortcuts on *Gmail*, *Google Docs* and *Google Sheets* are known to be broken.

**Update**: The change, originally requested by Google, has been temporarily [backed out](https://bugzilla.mozilla.org/show_bug.cgi?id=1443117) to give Google engineers time to fix the issue in their apps.

**Update 2**: This change has been landed again at Firefox 61 Nightly but disabled for now on *Gmail*, *Google Docs*, *Google Sheets* and *Google Slides* to avoid any breakage.

**Update 3**: *Google Hangouts*, *Google Inbox* and *Google Keep* as well as major public *Etherpad* instances have also been added to the blacklist so those developers have extra time to fix the issue.
