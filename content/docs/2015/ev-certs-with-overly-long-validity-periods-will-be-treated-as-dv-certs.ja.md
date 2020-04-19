---
title: "極端に有効期間が長い EV 証明書は DV 証明書として扱われます"
date: "2015-08-05T00:48:18-04:00"
categories: ["privacy-security"]
tags: []
releases: ["42", "45-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1145679"
      title: "Bug 1145679 - Reject EV status for end-entity EV certs with overly long validity periods"
---
EV SSL 証明書ガイドラインの現行版によれば、EV 証明書を 27 か月以上有効とすることはできません。Firefox は、後方互換性と近い将来の期限延長の可能性を考慮し、上限を 39 か月に設定しました。このため、39 か月以上の有効期間を持った EV 証明書は EV ステータスを拒絶され、通常の DV 証明書として扱われます。

**更新**: [Firefox 45](https://www.fxsitecompat.dev/ja/docs/2015/ev-certs-valid-for-more-than-27-months-will-be-treated-as-dv-certs/) で、この許容有効期間が 27 か月に短縮されました。
