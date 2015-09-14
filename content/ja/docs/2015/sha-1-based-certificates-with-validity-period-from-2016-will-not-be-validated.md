---
title: "2016 年からの有効期限が設定された SHA-1 ベースの証明書は認証されません"
date: "2015-09-13T21:46:00-04:00"
categories: ["privacy-security"]
tags: []
versions: "43"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=942515": "Bug 942515 - Show Untrusted Connection Error for SHA-1-based SSL certificates with notBefore >= 2016-01-01"
    "https://blog.mozilla.org/security/2014/09/23/phasing-out-certificates-with-sha-1-based-signature-algorithms/": "Phasing Out Certificates with SHA-1 based Signature Algorithms"
---
[弱い SHA-1 ハッシュアルゴリズム](https://developer.mozilla.org/docs/Web/Security/Weak_Signature_Algorithm) を使った証明書への対応は [Firefox 36 以降廃止予定とされています](https://www.fxsitecompat.com/ja/docs/2014/sha-1-support-has-been-deprecated/)。その廃止プロセスの一環として、<time datetime="2016-01-01">2016 年 1 月 1 日</time>以降に始まる有効期間が設定された SHA-1 ベースの証明書は Firefox 43 およびそれ以降のバージョンでは有効とみなされず、そうした証明書を使ったサイトでは「[接続の安全性を確認できません](https://support.mozilla.org/ja/kb/connection-untrusted-error-message)」という警告ページが表示されます。

Web マスターの皆さんは、[Web コンソール](https://developer.mozilla.org/ja/docs/Tools/Web_Console) を開き、あなたのサイトを読み込んで SHA-1 ベースの証明書が使われていないことを確認してください。もし SHA-1 ベースの証明書が使われているという警告がコンソールに表示された場合は、有効期間にかかわらずその発行者に連絡を取り、新しい SHA-1 ベースのものと無償で交換してください。Firefox は、他のブラウザとともに、<time datetime="2017-01">2017 年 1 月</time>以降すべての SHA-1 ベースの証明書について警告ページを表示する予定です。
