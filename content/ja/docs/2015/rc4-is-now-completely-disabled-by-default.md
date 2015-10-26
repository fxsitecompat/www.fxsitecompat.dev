---
title: "RC4 が初期設定で完全に無効化されました"
date: "2015-10-20T14:47:00-07:00"
categories: ["privacy-security"]
tags: []
versions: ["44"]
statuses: "affected"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=999544": "Bug 999544 - RC4 Considered Harmful: Disable use of RC4 completely (RFC 7465)"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1201025": "Bug 1201025 - Disable fallback whitelist by default, in all releases"
    "https://blog.mozilla.org/security/2015/09/11/deprecating-the-rc4-cipher/": "Deprecating the RC4 Cipher"
    "https://groups.google.com/d/topic/mozilla.dev.platform/JIEFcrGhqSM/discussion": "Intent to ship: RC4 disabled by default in Firefox 44"
---
Mozilla と他の主要ブラウザベンダーは、<time datetime="2016">2016 年</time> の早い時期に、[Firefox 36 以降廃止予定となっている](https://www.fxsitecompat.com/ja/docs/2014/rc4-support-has-been-deprecated/) 安全でない RC4 暗号化スイートへの対応を中止することで合意しました。

[廃止計画](https://groups.google.com/d/topic/mozilla.dev.platform/JIEFcrGhqSM/discussion) に従い、特定のサイトに RC4 の使用を許容する [ホワイトリスト](https://dxr.mozilla.org/mozilla-central/source/security/manager/ssl/IntolerantFallbackList.inc) が Firefox 44 で無効化され、RC4 が有効になっているどのサイトでも [信頼できない接続](https://support.mozilla.org/ja/kb/connection-untrusted-error-message) のエラーメッセージが表示されるようになります。Web 担当者は、早急にサーバを更新し、より強力な暗号化スイートを使用しなくてはなりません。
