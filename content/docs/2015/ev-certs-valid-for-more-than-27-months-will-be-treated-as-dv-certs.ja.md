---
title: "有効期間が 27 か月以上の EV 証明書は DV 証明書として扱われます"
date: "2015-11-16T22:08:00-08:00"
categories: ["privacy-security"]
tags: []
versions: ["45", "45-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1222903"
      title: "Bug 1222903 - Reject EV status for EV EE certs that are valid for longer than 27 months as well"
---
[Firefox 42](https://www.fxsitecompat.dev/ja/docs/2015/ev-certs-with-overly-long-validity-periods-will-be-treated-as-dv-certs/) 以降、有効期間が 39 か月以上の EV 証明書は DV 証明書として扱われてきました。Firefox 45 では、この許容有効期間が 27 か月に短縮されました。EV SSL 証明書ガイドラインが更新されてこの期間が 39 か月に延長される見込みが低いためです。
