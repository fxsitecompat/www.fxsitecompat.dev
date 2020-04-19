---
title: "Firefox 61 Developer Edition, upcoming keyboard event changes, and proper offline support"
date: "2018-05-09T21:37:00-04:00"
aliases:
    - "/en-CA/blog/2018/firefox-61-developer-edition-upcoming-keyboard-event-changes-and/"
---
Mozilla has shipped [Firefox 61 Beta and Developer Edition](https://www.mozilla.org/firefox/channel/desktop/). Check out our [Firefox 61 compatibility notes](https://www.fxsitecompat.dev/en-CA/releases/61/) to get prepared for the final version coming late June.

There are 2 upcoming changes in the browser's keyboard event handling. While the [first one](https://www.fxsitecompat.dev/en-CA/docs/2018/keydown-and-keyup-events-will-soon-be-fired-during-ime-composition/) may potentially affect applications serving East Asian users, the [second one](https://www.fxsitecompat.dev/en-CA/docs/2018/non-printable-keys-will-soon-stop-firing-keypress-event/) is known to break even major applications like *Google Docs*. Web developers are strongly encouraged to check them out and test the new behaviour with one of the [pre-release builds](https://www.mozilla.org/firefox/channel/desktop/).

[Another notable change](https://www.fxsitecompat.dev/en-CA/docs/2018/online-offline-events-are-no-longer-fired-on-document-and-document-body/) involves the `online` and `offline` events, which are no longer fired on `document`. Since some code snippets and documents, including a relevant MDN article, are written based on the previous wrong implementation, this change may impact certain web apps with offline capability. Luckily the solution is pretty simple: just replace `document` with `window`.
