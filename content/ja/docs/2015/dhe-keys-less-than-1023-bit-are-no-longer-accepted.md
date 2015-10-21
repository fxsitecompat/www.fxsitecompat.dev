---
title: "1023 ビット未満の DHE キーは受け入れられなくなりました"
date: "2015-03-17T14:02:59-04:00"
categories: ["privacy-security"]
tags: []
versions: ["39"]
statuses: "affected"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1138554": "Bug 1138554 – NSS accepts export-length DHE keys with regular DHE cipher suites"
    "http://www.mozilla-japan.org/security/announce/2015/mfsa2015-70.html": "MFSA 2015-70 – NSS の通常 DHE 暗号化スイートで輸出長の DHE 鍵が許容されている"
---
いわゆる「[Logjam](http://japan.zdnet.com/article/35064803/)」中間者攻撃を防ぐため、Firefox が対応する一時的ディフィー・ヘルマン (DHE) 鍵の低強度が 1023 ビットに制限されました。512 ビットの輸出グレード暗号は Mozilla 製品では使用不可となり、ユーザはそうした弱い鍵を提供しているサイトでは以下のようなエラーメッセージに遭遇するでしょう。

**更新**: [Firefox Input](https://input.mozilla.org/ja/?product=Firefox&q=ssl_error_weak_server_ephemeral_dh_key)、[Firefox Support](https://support.mozilla.org/ja/search?q=ssl_error_weak_server_ephemeral_dh_key) その他の情報源によれば、一定数のサイトがこの変更による影響を受けていることが判明しています。Web マスターの皆さんは、訪問者の安全が確保されているかどうか、今一度確かめてください。この問題についてよく分からない場合は、エラーが発生していることをサーバ管理者に知らせてください。
