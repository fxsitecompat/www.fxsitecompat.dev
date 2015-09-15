---
title: "RC4 対応が廃止予定となりました"
date: "2014-12-19T11:15:21-05:00"
categories: ["privacy-security"]
tags: []
versions: "36"
statuses: "affected"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=947149": "Bug 947149 – Connection information claims RC4 is \"high grade\""
    "https://bugzilla.mozilla.org/show_bug.cgi?id=999544": "Bug 999544 – RC4 Considered Harmful: Proposal to disable use of RC4 completely"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1088915": "Bug 1088915 – Stop offering RC4 in the first handshakes"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1093595": "Bug 1093595 – Treat SSL3 and RC4 as broken"
---
RC4 暗号スイートはもはや安全とは見なされなくなりました。RC4 は TLS の初回ハンドシェイクでは提供されなくなり、Firefox のセキュリティ UI でも今後は「高度な暗号化」とは呼ばれず、逆に「暗号化の強度が十分でない」という表現に差し替えられました。RC4 対応は近い将来 Mozilla 製品から完全に削除されます。Web マスターの皆さんはできるだけ早くサーバを更新して、より強力な暗号スイートを採用してください。
