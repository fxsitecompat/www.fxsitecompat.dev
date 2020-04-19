---
title: "特権管理機能が無効化されました"
date: "2012-12-03T03:50:54-05:00"
categories: ["privacy-security"]
tags: []
releases: ["17"]
statuses: "reverted"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=757046"
      title: "Bug 757046 – Investigate interim solutions for enablePrivilege"
---
[Firefox 12](https://dev.mozilla.jp/2012/03/firefox-12-site-compatibility/) 以降非推奨となっている [特権管理機能](https://www.mozilla.org/projects/security/components/signed-scripts.html) (JavaScript 拡張仕様 `netscape.security.PrivilegeManager.enablePrivilege`) が無効化されました。隠し設定 `security.enablePrivilege.enable_for_tests` の値を `true` に変更すればこの機能をテストできますが、当然のことながら推奨されません。実際に特権が必要な場面ではアドオンなどの代替策を検討してください。

なお、ブラウザー判別にまだ `netscape.security` オブジェクトを使用しているサイトが確認されたため、[一時的にこのオブジェクトを復活させる措置](https://bugzilla.mozilla.org/show_bug.cgi?id=791526) を取っています。今後ブラウザー判別には別の方法を使用してください。
