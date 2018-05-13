---
title: "Showing dialogs are no longer allowed on page navigation events"
date: "2012-12-03T03:50:54-05:00"
categories: ["dom"]
tags: []
versions: ["17"]
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=391834"
      title: "Bug 391834 – Don\'t allow alert/confirm/prompt in onbeforeunload, onunload and onpagehide"
---
Scripts to show dialogs using the [`alert`](https://developer.mozilla.org/docs/Web/API/window.alert), [`confirm`](https://developer.mozilla.org/docs/Web/API/window.confirm) or [`prompt`](https://developer.mozilla.org/docs/Web/API/window.prompt) functions on the [`beforeunload`](https://developer.mozilla.org/docs/Web/Reference/Events/beforeunload), [`unload`](https://developer.mozilla.org/docs/Web/Reference/Events/unload) or [`pagehide`](https://developer.mozilla.org/docs/Web/Reference/Events/pagehide) events are now ignored. This is a way to protect against DoS attacks where a malicious site prevents browser to be closed using an infinite loop at the time of closing a tab, reloading a page or navigating to a different page.
