---
title: "Vibration API がクロスオリジン `<iframe>` から使用できなくなりました"
date: "2019-11-13T07:53:00-05:00"
categories: ["dom"]
tags: []
versions: ["72"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1591113"
      title: "Bug 1591113 - Remove support for third-party vibrate"
---
Firefox 72 以降、クロスオリジン `<iframe>` 内での [Vibration API](https://developer.mozilla.org/docs/Web/API/Vibration_API) の使用が許可されなくなりました。これは、この API が信頼できないサードパーティによってしばしば悪用されるためです。今後、そうした場合には、`navigator.vibrate` メソッドの呼び出しはエラーなしに失敗するようになります。Google Chrome は既にバージョン 55 で [同様の変更](https://www.chromestatus.com/feature/5682658461876224) を行っています。
