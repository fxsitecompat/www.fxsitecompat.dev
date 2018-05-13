---
title: "`-moz-transform` の旧式構文対応が廃止されました"
date: "2018-02-20T01:31:00-05:00"
categories: ["css"]
tags: []
versions: ["60"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1438297"
      title: "Bug 1438297 - Unship the legacy syntax for -moz-transform."
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/T3PGm97MPNU/discussion"
      title: "Intent to unship: Legacy -moz-transform syntax."
---
Firefox はこれまで、`matrix(1, 2, 3, 4, 5px, 6%)` のように `matrix` や `matrix3d` 関数に長さやパーセントの使用を許容していた、`-moz-transform` CSS プロパティの旧式構文対応を維持してきました。Firefox 60 以降、こうした特別なケースは処理されなくなり、`-moz` 接頭辞付きプロパティは `-webkit-transform` と同様に標準 [`transform`](https://developer.mozilla.org/docs/Web/CSS/transform) プロパティの単なるエイリアスとなります。

なお、`-moz-transform` 対応は [将来的に廃止されます](https://www.fxsitecompat.com/ja/docs/2015/prefixed-css-animations-transforms-transitions-support-will-be-removed/) ので、必ず標準のプロパティを使用するようにしてください。
