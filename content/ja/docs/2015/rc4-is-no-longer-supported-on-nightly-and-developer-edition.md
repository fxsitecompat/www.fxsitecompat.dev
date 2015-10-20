---
title: "Nightly と Developer Edition で RC4 対応が打ち切られました"
date: "2015-09-23T06:18:00-04:00"
categories: ["privacy-security"]
tags: []
versions: "42"
statuses: "affected"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1201023": "Bug 1201023 - Disable fallback whitelist in Nightly/DevEdition"
    "https://groups.google.com/d/topic/mozilla.dev.platform/JIEFcrGhqSM/discussion": "Intent to ship: RC4 disabled by default in Firefox 44"
---
Mozilla と他の主要ブラウザベンダーは、<time datetime="2016">2016 年</time> の早い時期に、[Firefox 36 以降廃止予定となっている](https://www.fxsitecompat.com/ja/docs/2014/rc4-support-has-been-deprecated/) 安全でない RC4 暗号化スイートへの対応をようやく中止することで合意しました。[廃止計画](https://groups.google.com/d/topic/mozilla.dev.platform/JIEFcrGhqSM/discussion) に従い、特定のサイトに RC4 の使用を許容する [ホワイトリスト](https://dxr.mozilla.org/mozilla-central/source/security/manager/ssl/IntolerantFallbackList.inc) が Firefox Nightly と Developer Edition で無効化されました。

Firefox 44 以降、RC4 対応はすべてのチャンネルで初期設定無効となります。Web 担当者は、早急にサーバを更新し、より強力な暗号化スイートを使用しなくてはなりません。
