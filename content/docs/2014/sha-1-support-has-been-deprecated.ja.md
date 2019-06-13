---
title: "SHA-1 対応が廃止予定となりました"
date: "2014-12-19T11:15:21-05:00"
categories: ["privacy-security"]
tags: []
versions: ["36"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1068949"
      title: "Bug 1068949 – Add SHA-1 warnings to web console for end entities"
---
[弱い SHA-1 ハッシュアルゴリズム](https://developer.mozilla.org/docs/Security/Weak_Signature_Algorithm) を使用した SSL 証明書への対応が廃止予定となりました。SHA-1 証明書が見つかった場合、[ウェブコンソールは警告を表示します](https://developer.mozilla.org/docs/Tools/Web_Console#Security_warnings_and_errors)。

**更新** SHA-1 対応は [2017 年 1 月に無効化されます](https://www.fxsitecompat.dev/ja/docs/2016/sha-1-certificates-issued-by-public-ca-will-no-longer-be-accepted/)。
