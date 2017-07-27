---
title: "Firefox OS API がウェブコンテンツから隠されました"
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
Firefox は、[Contacts](https://developer.mozilla.org/ja/docs/Mozilla/Firefox_OS/API/Contacts_API)、[Power Management](https://developer.mozilla.org/ja/docs/Mozilla/Firefox_OS/API/Power_Management_API)、[Settings](https://developer.mozilla.org/ja/docs/Mozilla/Firefox_OS/API/Settings_API) といった、いくつかの Firefox OS 内部アプリケーション向け非標準 Web API を誤って露呈していました。それらの API には適切な許可設定が必要とされるため、いずれにしても一般のウェブサイトやアプリケーションから使うことはできません。このため、以下のインターフェイスはウェブコンテンツから隠されるようになりました。[`mozContact`](https://developer.mozilla.org/ja/docs/Mozilla/Firefox_OS/API/MozContact)、[`MozContactChangeEvent`](https://developer.mozilla.org/ja/docs/Mozilla/Firefox_OS/API/MozContactChangeEvent)、[`navigator.mozContacts`](https://developer.mozilla.org/ja/docs/Web/API/Navigator/mozContacts)、[`MozPowerManager`](https://developer.mozilla.org/ja/docs/Mozilla/Firefox_OS/API/MozPowerManager)、[`MozSettingsEvent`](https://developer.mozilla.org/ja/docs/Mozilla/Firefox_OS/API/MozSettingsEvent)
