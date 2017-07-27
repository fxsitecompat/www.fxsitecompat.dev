---
title: "SSLv3 が無効化されました"
date: "2014-09-01T22:12:15-04:00"
categories: ["privacy-security"]
tags: []
versions: ["34"]
statuses: "affecting"
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1030963"
      title: "Bug 1030963 – (POODLE) Padding oracle attack on SSL 3.0"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1085138"
      title: "Bug 1085138 – (POODLEBITE) [META] Sites broken due to reliance on a security protocol that was obsolete last millennium"
---
Google によって報告された POODLE 攻撃への対応として、Firefox 34 (Beta 3 以降) では SSL バージョン 3.0 が初期設定で無効化されています。法人向けの [Firefox ESR](http://www.mozilla.jp/business/downloads/) もバージョン 31.3.0 で SSLv3 が無効化されます。バグのコメントによれば、Alexa 上位 100 万ドメインのうち約 1% が SSLv3 を必須としていることから、この変更による影響を受けるようです。SSLv3 を必須としているサイトは、できるだけ早く TLS の最近のバージョンへアップグレードしてください。詳しくは [Mozilla Security Blog](https://blog.mozilla.org/security/2014/10/14/the-poodle-attack-and-the-end-of-ssl-3-0/) をご覧ください。影響を受けるサイトを見つけたら [Bug 1085138 のブロッカー](https://bugzilla.mozilla.org/showdependencytree.cgi?id=1085138) として報告してください。
