---
title: "ログインフォームが含まれる非 HTTPS サイトは安全でないと表示されます"
date: "2015-10-21T14:38:00-07:00"
categories: ["privacy-security"]
tags: []
versions: ["46"]
statuses: "affected"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1188121": "Bug 1188121 - [userstory] CC: Warning for password on non-secure connection"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1179961": "Bug 1179961 - Use a lock with a strikethrough for HTTP pages that have Password Fields in the Control Center"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1221206": "Bug 1221206 - Turn on Insecure Password Warning for Firefox Dev Edition"
---
現在表示されているページに `<input type="password">` が含まれていて、なおかつ接続が安全でない場合、Firefox はロケーションバーに [壊れた南京錠アイコン](https://bug1179961.bmoattachments.org/attachment.cgi?id=8662392) を表示するようになりました。パスワードが送信されるページだけでなく、ログインフォームが存在するページ自体も、[リモートの攻撃者からユーザのログイン情報を保護する](https://developer.mozilla.org/ja/docs/Web/Security/Insecure_passwords) ため HTTPS プロトコルを使用すべきです。

この機能は今のところ Firefox Nightly と Developer Edition のみで有効化されていますが、Web マスターの皆さんはそうした気まずい状況を避けたいと思うでしょう。TLS 証明書を購入する予算がありませんか？ 心配ありません。2015 年 11 月以降、Mozilla などが運営する新しい認証局 [Let's Encrypt](https://letsencrypt.org/) が、信頼の置ける証明書を無償で提供します。
