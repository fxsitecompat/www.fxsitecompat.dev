---
title: "MD5 証明書の受け入れが中止されました"
date: "2012-10-09T06:00:00-04:00"
categories: ["privacy-security"]
tags: []
releases: ["16"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=650355"
      title: "Bug 650355 – Stop accepting MD5 as a hash algorithm in signatures (toggle security.enable_md5_signatures to false)"
---
MD5 ハッシュアルゴリズムは [安全でない](https://developer.mozilla.org/docs/Web/Security/Weak_Signature_Algorithm) ことから、Firefox 16 以降無効化する措置が取られました。MD5 アルゴリズムで署名された SSL 証明書を使用しているサイトを Firefox で開こうとするとエラー画面が表示されます。便宜的に、ユーザーが [このエラーを無視する](https://bugzilla.mozilla.org/show_bug.cgi?id=758314) こともまだ可能となっています。
