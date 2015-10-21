---
title: "Windows 64 ビット版 Firefox が一般公開、対応プラグインは Flash のみとなります"
date: "2015-06-13T15:20:46-04:00"
categories: ["plugins"]
tags: []
versions: ["42"]
statuses: "affected"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1180792": "Bug 1180792 - enable 64-bit windows builds on release channel"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1181014": "Bug 1181014 - Make Firefox 42 win64 builds on the Release channel available on mozilla.org"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1165981": "Bug 1165981 - Whitelist Flash for NPAPI on 64 bit Firefox on Win64"
---
Windows 向け Firefox 64 ビット版はしばらく前から [Developer Edition](https://www.mozilla.org/ja/firefox/developer/all/) と [Beta](https://www.mozilla.org/ja/firefox/beta/all/) でテスト用に公開されてきましたが、Firefox 42 以降、64 ビット版は Release (安定版) チャンネルを通じて一般に公開されます。つまり、より多くのユーザが 64 ビット版を使い始めるということで、あなたのサイトで提供しているコンテンツが 32 ビット版 [NPAPI プラグイン](https://developer.mozilla.org/ja/Add-ons/Plugins) を必要とする場合、それらの Firefox ユーザは使用できないことになります。今のところ Adobe Flash Player が 64 ビット版で唯一の対応プラグインとなっています。コンテンツ提供者には、プラグインへの依存をやめ、[最新 Web 技術](https://developer.mozilla.org/ja/docs/Web) を採用するよう強く推奨します。

**更新**: Mozilla が「パートナー関連のいくつかの変更を待っている」ため、Windows 64 ビット版の一般公開は延期されました。現時点でのスケジュールは不明です。
