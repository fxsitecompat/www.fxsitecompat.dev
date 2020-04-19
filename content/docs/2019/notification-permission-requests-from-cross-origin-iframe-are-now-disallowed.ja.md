---
title: "クロスオリジン `<iframe>` からの通知許可リクエストが禁止されました"
date: "2019-08-13T14:24:00-04:00"
categories: ["dom"]
tags: []
releases: ["70"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1560741"
      title: "Bug 1560741 - Disallow notification permission requests from cross-origin iframes"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/-6HYtlHuYO8/discussion"
      title: "Intent to ship: restrict access to request notification permissions from cross-origin iframes"
---
Firefox 70 以降、クロスオリジン `<iframe>` から `Notification.requestPermission` メソッドが呼ばれた場合、デスクトップ通知許可のリクエストはすべて却下されます。ブロックされた際にプロンプトは表示されず、ウェブコンソールに警告が出力されます。Mozilla の Telemetry によれば、そうした許可リクエストは 0.03% 以下となっており、互換性リスクは非常に低いはずです。

将来的には同一オリジン `<iframe>` からのリクエストも却下される可能性があります。許可が必要な場合には、必ずトップレベルドキュメントからリクエストを出すようにしましょう。
