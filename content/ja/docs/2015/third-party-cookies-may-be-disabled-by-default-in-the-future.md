---
title: "サードパーティ Cookie は将来的に初期設定で無効化される可能性があります"
date: "2015-10-27T14:54:00-07:00"
categories: ["networking", "privacy-security"]
tags: []
versions: ["future"]
statuses: "affected"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=818340": "Bug 818340 - Block cookies from sites I haven't visited"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=851606": "Bug 851606 - Disable bug 818340 for Beta until we're ready"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=999170": "Bug 999170 - Back out bug 851606 to enable bug 818340 on the default 3rd-party cookie policy for releases"
---
[サードパーティ Cookie](https://support.mozilla.org/ja/kb/disable-third-party-cookies) とプライバシーに関しては長いこと議論が続いています。この変更は [元々 Firefox 22 で予定されていました](https://www.fxsitecompat.com/ja/docs/2013/third-party-cookies-are-blocked-by-default/) が、明らかな互換性問題から Beta、Release 両チャンネルでは取り消されました。[Developer Edition](https://www.mozilla.org/ja/firefox/developer/) と Nightly チャンネルではサードパーティ Cookie は初期設定で無効となっており、関連バグはまだ開かれたままとなっています。また [Firefox 42 にはトラッキング保護機能付きプライベートブラウジングも搭載されています](https://www.fxsitecompat.com/ja/docs/2015/private-browsing-now-comes-with-tracking-protection/)。まだはっきりとしたスケジュールは出されていませんが、このトピックは注目に値するでしょう。
