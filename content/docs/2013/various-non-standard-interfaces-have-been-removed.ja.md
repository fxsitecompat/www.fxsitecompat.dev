---
title: "様々な非標準インターフェイスが削除されました"
date: "2013-09-19T23:58:13-04:00"
categories: ["dom"]
tags: []
releases: ["26", "31-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=899388"
      title: "Bug 899388 – Remove XUL-related interfaces and ChromeWindow from content"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=909340"
      title: "Bug 909340 – Hide XULElement from content"
---
グローバルオブジェクトを標準化する継続的な取り組みの一環として、次の非標準 [XUL](https://developer.mozilla.org/docs/XUL) 関連インターフェイスが削除されました。`ChromeWindow`、`XULButtonElement`、`XULCheckboxElement`、`XULCommandDispatcher`、`XULCommandEvent`、`XULControlElement`、`XULDocument`、`XULElement`、`XULLabeledControlElement`、`XULPopupElement`
