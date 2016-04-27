---
title: "`<isindex>` 対応が廃止されます"
date: "2016-04-26T21:50:00-04:00"
categories: ["html"]
tags: []
versions: ["future"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1266495"
      title: "Bug 1266495 - Consider removing <isindex> from the parser and form submission"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/DV3YBf7wI3M/discussion"
      title: "Intent to remove: <isindex>"
---
時代遅れとなった [`<isindex>`](https://developer.mozilla.org/ja/docs/Web/HTML/Element/isindex) 要素と `<input name="isindex">` が HTML 標準から削除されました。Google Chrome と Microsoft Edge はもうこれらに対応しておらず、Firefox もまもなくこのレガシーな機能を削除します。
