---
title: "HTTP Public Key Pinning への対応が打ち切られました"
date: "2019-11-14T16:54:00-05:00"
categories: ["networking", "privacy-security"]
tags: []
releases: ["72"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1412438"
      title: "Bug 1412438 - consider removal of HTTP Public Key Pinning (HPKP)"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/AyMlrNHYepE/discussion"
      title: "intent to unship: HPKP (dynamic key pinning)"
---
Firefox 72 で、低い採用率や相互運用性リスクを理由として、[HTTP Public Key Pinning](https://developer.mozilla.org/docs/Web/HTTP/Public_Key_Pinning) (HPKP) への対応が廃止されました。Google Chrome は既にバージョン 72 で [対応を廃止](https://www.chromestatus.com/feature/5903385005916160) しており、他のブラウザーはこのセキュリティ機能に対応していないことから、誤設定されたり一時的にクラッキングされたりしたサイトが Firefox でのみブロックされ、ユーザー体験の低下をもたらす可能性がありました。今後 `Public-Key-Pins` HTTP レスポンスヘッダーは単純に無視されます。
