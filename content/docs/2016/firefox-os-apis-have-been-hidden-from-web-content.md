---
title: "Firefox OS APIs have been hidden from Web content"
date: "2016-03-16T12:14:00-04:00"
categories: ["dom"]
tags: []
versions: ["48"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1043562"
      title: "Bug 1043562 - Remove the dom.mozContacts.enabled pref and hide the MozContact API from code with insufficient privileges"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1256046"
      title: "Bug 1256046 - Hide MozPowerManager from the Web"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1256414"
      title: "Bug 1256414 - Hide MozSettingsEvent from the Web"
---
Firefox was erroneously exposing several non-standard Web APIs intended for Firefox OS internal applications, including [Contacts](https://developer.mozilla.org/en-US/docs/Mozilla/Firefox_OS/API/Contacts_API), [Power Management](https://developer.mozilla.org/en-US/docs/Mozilla/Firefox_OS/API/Power_Management_API) and [Settings](https://developer.mozilla.org/en-US/docs/Mozilla/Firefox_OS/API/Settings_API). Those APIs cannot be used by general Web sites and applications anyway because appropriate permissions are required. Therefore, the following interfaces are now hidden from Web content: [`mozContact`](https://developer.mozilla.org/en-US/docs/Mozilla/Firefox_OS/API/MozContact), [`MozContactChangeEvent`](https://developer.mozilla.org/en-US/docs/Mozilla/Firefox_OS/API/MozContactChangeEvent), [`navigator.mozContacts`](https://developer.mozilla.org/en-US/docs/Web/API/Navigator/mozContacts), [`MozPowerManager`](https://developer.mozilla.org/en-US/docs/Mozilla/Firefox_OS/API/MozPowerManager), [`MozSettingsEvent`](https://developer.mozilla.org/en-US/docs/Mozilla/Firefox_OS/API/MozSettingsEvent)
