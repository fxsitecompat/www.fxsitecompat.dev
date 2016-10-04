---
title: "CSP ポリシー命令文内のワイルドカードが `blob:`、`data:`、`filesystem:` のリソースを許容しなくなりました"
date: "2015-04-27T13:17:23-04:00"
categories: ["privacy-security"]
tags: []
versions: ["40"]
statuses: "affecting"
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1086999"
      title: "Bug 1086999 - CSP: Asterisk (*) wildcard should not allow blob:, data:, or filesystem: when matching source expressions"
    - url: "http://www.mozilla-japan.org/security/announce/2015/mfsa2015-91.html"
      title: "MFSA 2015-91 - Mozilla の Content Security Policy 実装が仕様に反してアスタリスクワイルドカードを許容している"
---
Firefox は、[CSP ポリシー命令文](https://developer.mozilla.org/ja/docs/Web/Security/CSP/CSP_policy_directives) 内でアスタリスクワイルドカード (`*`) が使われていた場合に、`blob:`、`data:`、`filesystem:` URL からのリソースを誤って許可していました。この挙動は Firefox 40 で修正されました。これまでに [*CNN*](https://bugzilla.mozilla.org/show_bug.cgi?id=1155792)、[*Facebook*](https://bugzilla.mozilla.org/show_bug.cgi?id=1181379)、[*FastMail*](https://bugzilla.mozilla.org/show_bug.cgi?id=1157084)、[*WhatsApp*](https://bugzilla.mozilla.org/show_bug.cgi?id=1154704) がこの変更の影響を受けていることが判明しています。それらのサイトはポリシー命令文に `img-src: *` を含みつつ `data:` URL で画像を表示しているようです。この問題の解決策は、該当する命令文に明示的に `data:` を追加することです。
