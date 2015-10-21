---
title: "プラグインホワイトリストが実装されました"
date: "2014-03-21T04:50:04-04:00"
categories: ["plugins"]
tags: []
versions: ["30"]
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=992995": "Bug 992995 – Implement plugin whitelist"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1007389": "Bug 1007389 – Implement plugin whitelist, round 2"
---
[Firefox 26](https://www.fxsitecompat.com/ja/docs/2013/java-is-now-defaulted-to-click-to-activate/) に Click-to-Activate (クリックで有効化) 機能が追加されて以来、Mozilla は [プラグインホワイトリストポリシー](https://blog.mozilla.org/security/2014/02/28/update-on-plugin-activation/) を定義してきました。ホワイトリストは Firefox 30 に実装され、プラグインは登録済みのものを除き初期設定で Click-to-Activate が適用されるようになりました。ホワイトリストに登録されているプラグインの完全な一覧は [このスプレッドシート](https://docs.google.com/spreadsheets/d/19JIQiaS9mJgkKQ07ax2KH7syRCgxt2dCCxcBD56PiQc/edit?usp=sharing) を参照してください。
