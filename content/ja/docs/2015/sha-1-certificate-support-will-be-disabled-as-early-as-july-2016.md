---
title: "SHA-1 証明書対応は早ければ 2016 年 7 月にも無効化されます"
date: "2015-10-25T13:37:00-07:00"
categories: ["privacy-security"]
tags: []
versions: ["future"]
statuses: "affecting"
references:
    - url: "https://groups.google.com/d/topic/mozilla.dev.security.policy/wXvLQ26JyOA/discussion"
      title: "mozilla.dev.security.policy: Update to phasing out SHA-1 Certs"
    - url: "https://blog.mozilla.org/security/2015/10/20/continuing-to-phase-out-sha-1-certificates/"
      title: "Continuing to Phase Out SHA-1 Certificates"
---
[弱い SHA-1 ハッシュアルゴリズム](https://developer.mozilla.org/docs/Web/Security/Weak_Signature_Algorithm) を使った SSL 証明書への対応は [Firefox 36 以降廃止予定とされています](https://www.fxsitecompat.com/ja/docs/2014/sha-1-support-has-been-deprecated/)。<time datetime="2016-01">2016 年 1 月</time> 以降に発行された SHA-1 証明書は [受け入れられず](https://www.fxsitecompat.com/ja/docs/2015/sha-1-based-certificates-with-validity-period-from-2016-will-not-be-validated/)、[信頼できない接続](https://support.mozilla.org/ja/kb/connection-untrusted-error-message) エラーが表示されます。

Mozilla の廃止計画によれば <time datetime="2017-01">2017 年 1 月</time> 以降 SHA-1 証明書はすべて拒絶されますが、SHA-1 に対する最近の攻撃を受けて、この日付は <time datetime="2016-07">2016 年 7 月</time> に前倒しされる可能性があります。

[4 分の 1 以上のサイト](http://news.netcraft.com/archives/2015/10/19/one-million-ssl-certificates-still-using-insecure-sha-1-algorithm.html) が未だに SHA-1 証明書を採用しています。[ウェブコンソール](https://developer.mozilla.org/ja/docs/Tools/Web_Console) であなたのサイトを読み込んで SHA-1 証明書についての警告が表示された場合は、その発行者へ速やかに連絡を取り、有効期間に関わらず新しい SHA-2 証明書と無償で交換してください。
