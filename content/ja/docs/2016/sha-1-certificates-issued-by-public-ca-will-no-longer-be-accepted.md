---
title: "公的認証局によって発行された SHA-1 証明書は受け入れられなくなります"
date: "2016-10-24T13:13:00-04:00"
categories: ["privacy-security"]
tags: []
versions: ["52"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1302140"
      title: "Bug 1302140 - add policy mode to completely disallow sha-1 signature except for certificates issued by non-built-in roots"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1321114"
      title: "Bug 1321114 - Remote SHA-1 shut-off"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1330043"
      title: "Bug 1330043 - disable sha1 in signatures on certificates issued by publicly-trusted roots"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1339646"
      title: "Bug 1339646 - Broken sites due to SHA1-encoded intermediate certs"
    - url: "https://groups.google.com/d/topic/mozilla.dev.security.policy/wXvLQ26JyOA/discussion"
      title: "mozilla.dev.security.policy: Update to phasing out SHA-1 Certs"
    - url: "https://blog.mozilla.org/security/2015/10/20/continuing-to-phase-out-sha-1-certificates/"
      title: "Continuing to Phase Out SHA-1 Certificates"
    - url: "https://blog.mozilla.org/security/2016/10/18/phasing-out-sha-1-on-the-public-web/"
      title: "Phasing Out SHA-1 on the Public Web"
    - url: "https://blog.mozilla.org/security/2017/02/23/the-end-of-sha-1-on-the-public-web/"
      title: "The end of SHA-1 on the Public Web"
aliases:
    - "/docs/2015/sha-1-certificate-support-will-be-disabled-as-early-as-july-2016/"
---
[弱い SHA-1 ハッシュアルゴリズム](https://developer.mozilla.org/docs/Web/Security/Weak_Signature_Algorithm) を使った SSL 証明書への対応は [Firefox 36 以降廃止予定とされています](https://www.fxsitecompat.com/ja/docs/2014/sha-1-support-has-been-deprecated/)。Firefox 48 以降では、<time datetime="2016-01">2016 年 1 月</time>以降に発行された SHA-1 証明書は、手作業でインポートされたルート証明書を除き [受け入れられません](https://www.fxsitecompat.com/ja/docs/2015/sha-1-based-certificates-with-validity-period-from-2016-will-not-be-validated/)。

<time datetime="2017-04">2017 年 4 月</time>公開の Firefox 53 でこの期間条件がなくなり、公的認証局によって発行された SHA-1 証明書はすべて [信頼できない接続](https://support.mozilla.org/ja/kb/connection-untrusted-error-message) エラー表示となります。[Mozilla の発表](https://blog.mozilla.org/security/2016/10/18/phasing-out-sha-1-on-the-public-web/) によれば、現在の SHA-1 使用率は 1% 未満であり、対応の廃止は Firefox 51 Beta サイクル中に影響を評価しつつ徐々に拡大されます。

[ウェブコンソール](https://developer.mozilla.org/ja/docs/Tools/Web_Console) であなたのサイトを読み込んで SHA-1 証明書についての警告が表示された場合は、その発行者へ速やかに連絡を取り、有効期間に関わらず新しい SHA-2 証明書と無償で交換してください。

**更新**: 影響を受けるバージョンを修正しました。Firefox 51 ではなく 53 です。

**更新 2**: [Google Chrome 56](https://security.googleblog.com/2016/11/sha-1-certificates-in-chrome.html) が 2017 年 1 月に既に SHA-1 対応を廃止していることから、Mozilla は 3 月公開の Firefox 52 で [この変更を前倒しで行う](https://mail.mozilla.org/pipermail/gofaster/2017-February/000563.html) ことを予定しています。それに伴い、この記事のバージョンを再度変更しました。

**更新 3**: バグの [コメント](https://bugzilla.mozilla.org/show_bug.cgi?id=1330043#c15) によれば、証明書の交換後もまだ Firefox でエラーページが見られる場合は、中間証明書も認証局 (CA) によって近年再発行された可能性があり、それらも併せて更新する必要があるかもしれません。他のブラウザーは、その方針によっては、そうした場合に何もエラーを出さない場合があります。[影響を受けるサイト一覧](https://bug1339646.bmoattachments.org/attachment.cgi?id=8837360) を参照してください。

**更新 4**: Google による [初の現実的な SHA-1 衝突](https://security.googleblog.com/2017/02/announcing-first-sha1-collision.html) の発表を受けて、Mozilla は <time datetime="2017-03-07">2017 年 3 月 7 日</time>の Firefox 52 最終リリースを待つことなく、<time datetime="2017-02-24">2 月 24 日</time>にリモートですべての Firefox ユーザーの SHA-1 対応を無効化しました。
