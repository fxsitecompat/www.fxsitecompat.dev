---
title: "RC4 はホワイトリスト掲載サイトに限って許容されるようになりました"
date: "2015-09-25T00:54:00-04:00"
categories: ["privacy-security"]
tags: []
versions: ["43"]
statuses: "reverted"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1201024"
      title: "Bug 1201024 - Disable unrestricted RC4 fallback"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/JIEFcrGhqSM/discussion"
      title: "Intent to ship: RC4 disabled by default in Firefox 44"
---
Mozilla と他の主要ブラウザーベンダーは、<time datetime="2016">2016 年</time> の早い時期に、[Firefox 36 以降廃止予定となっている](https://www.fxsitecompat.com/ja/docs/2014/rc4-support-has-been-deprecated/) 安全でない RC4 暗号化スイートへの対応をようやく中止することで合意しました。[廃止計画](https://groups.google.com/d/topic/mozilla.dev.platform/JIEFcrGhqSM/discussion) に従い、特定のサイトに RC4 の使用を許容する [ホワイトリスト](https://dxr.mozilla.org/mozilla-central/source/security/manager/ssl/IntolerantFallbackList.inc) が、Firefox Nightly と Developer Edition に加えて、Beta、Release 両チャンネルにも適用されました。つまり、ホワイトリストに掲載されておらず RC4 が有効になっている様々なサイトで [信頼できない接続](https://support.mozilla.org/kb/connection-untrusted-error-message) のエラーメッセージが表示されるようになります。

Firefox 44 以降、RC4 対応はすべてのチャンネルで初期設定無効となります。ウェブ担当者は、早急にサーバーを更新し、より強力な暗号化スイートを使用しなくてはなりません。

**更新**: この変更は、RC4 の一時的な使用を許可する UI がまだ整っていないため [取り消されました](https://bugzilla.mozilla.org/show_bug.cgi?id=1207257)。
