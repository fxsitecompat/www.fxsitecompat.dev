---
title: "接頭辞付き Page Visibility API が削除されました"
date: "2016-09-07T18:11:00-04:00"
categories: ["dom"]
tags: []
versions: ["51", "52-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=812701"
      title: "Bug 812701 - Drop the prefixed version of visibility API"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/FkAJkVOJF74/discussion"
      title: "Intent to unship: -moz-prefixed Page Visibility API."
aliases:
    - "/ja/docs/2015/prefixed-page-visibility-api-will-be-removed/"
    - "/ja/docs/2016/prefixed-page-visibility-api-has-been-be-removed/"
---
[Firefox 18 以降廃止予定となっていた](https://www.fxsitecompat.dev/ja/docs/2012/page-visibility-api-has-been-unprefixed/) 接頭辞付き [Page Visibility API](https://developer.mozilla.org/docs/Web/API/Page_Visibility_API) への対応が Firefox 51 で削除されました。これには、`mozHidden`、`mozVisibilityState` 両プロパティおよび `mozvisibilitychange` イベントが含まれます。接頭辞の外れた標準のプロパティやイベントで代用してください。
