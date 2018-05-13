---
title: "`-moz-user-input:enabled` と `disabled` への対応が廃止されました"
date: "2018-02-16T10:39:00-05:00"
categories: ["css"]
tags: []
versions: ["60"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1405087"
      title: "Bug 1405087 - JavaScript: The \"click ()\" event isn`t executing from the script after deleting/setting to \"false\" the \"disabled\" prop of the element \"input type = submit\""
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/E6tfP__wkwg/discussion"
      title: "Intent to unship: -moz-user-input: disabled / enabled"
---
非標準 CSS プロパティ [`-moz-user-input`](https://developer.mozilla.org/docs/Web/CSS/-moz-user-input) の値のうち、`enabled` と `disabled` への対応が Firefox 60 で削除されました。これらはめったに使われておらず、実際のところ動的に変更された場合には正常に動作していませんでした。`none` と既定値 `auto` への対応は残されていますが、プロパティ自体今後完全に削除される可能性があります。他のどのブラウザーもこのプロパティに対応していないことから、互換性リスクは低いはずです。
