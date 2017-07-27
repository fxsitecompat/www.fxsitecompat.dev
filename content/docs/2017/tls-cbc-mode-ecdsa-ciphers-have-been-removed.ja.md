---
title: "TLS の CBC モード ECDSA 暗号が削除されました"
date: "2017-03-11T21:42:00-05:00"
categories: ["privacy-security"]
tags: []
versions: ["53"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1316300"
      title: "Bug 1316300 - Deprecate and remove: TLS CBC-mode ECDSA cipher suites"
---
めったに使われていない TLS 1.3 の CBC モード ECDSA 暗号スイートへの対応が Firefox 53 で削除されました。既に [Chrome 56](https://www.chromestatus.com/feature/5740978103123968) が今年 1 月に削除しており、互換性リスクは低いはずです。
