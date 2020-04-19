---
title: "リモート JAR 対応が再度無効化されました"
date: "2017-04-05T08:46:00-04:00"
categories: ["networking", "privacy-security"]
tags: []
versions: ["55", "60-esr"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1255139"
      title: "Bug 1255139 - iNotes not working after upgrade to release 45.0"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1329336"
      title: "Bug 1329336 - Disable loading remote jars by default"
---
セキュリティ上の理由から、初期設定で Java アーカイブ (JAR) をリモートの場所から読み込むことはできなくなりました。この変更は元々 [Firefox 45](https://www.fxsitecompat.dev/ja/docs/2015/jar-protocol-support-has-been-disabled-by-default/) で行われましたが、*IBM iNotes* に影響があったためすぐに取り消されていました。当該製品は [2016 年 5 月に更新され](https://www-10.lotus.com/ldd/fixlist.nsf/8d1c0550e6242b69852570c900549a74/e413ea1ca447b3bf85257f77006b7f60) Firefox 向けに JAR を使わないようになったことから、Firefox 55 で再度無効化が試みられることとなりました。

*iNotes* ユーザーは Fix Pack をインストールして互換性問題を解決してください。何らかの理由でインスタンスをすぐに更新できない場合は、Firefox 52 [延長サポート版](https://www.mozilla.org/firefox/organizations/) を使えば 2018 年 <del>第 2 四半期</del> <ins>8 月</ins> までリモート JAR 対応が有効となります。

JAR に対応しているブラウザーは他にありません。また今のところ他に影響を受けるアプリは報告されていません。

**更新** リモート JAR 対応は [Firefox 61 で完全に廃止されました](https://www.fxsitecompat.dev/ja/docs/2018/remote-jar-support-has-been-completely-removed/).
