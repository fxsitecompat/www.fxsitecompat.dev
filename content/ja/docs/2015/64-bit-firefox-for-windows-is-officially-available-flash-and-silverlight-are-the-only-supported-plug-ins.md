---
title: "Windows 64 ビット版 Firefox が正式公開、対応プラグインは Flash、Silverlight のみとなります"
date: "2015-06-13T15:20:46-04:00"
categories: ["plugins"]
tags: []
versions: ["43"]
statuses: "affecting"
cclicense: "BY-SA 3.0"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1180792"
      title: "Bug 1180792 - enable 64-bit windows builds on release channel"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1229852"
      title: "Bug 1229852 - Add Firefox Win64 download to /firefox/all/"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1165981"
      title: "Bug 1165981 - Whitelist Flash for NPAPI on 64 bit Firefox on Win64"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1225293"
      title: "Bug 1225293 - Support Silverlight for Win64 Firefox"
aliases:
    - "/docs/2015/64-bit-firefox-for-windows-is-publicly-available-only-flash-is-supported/"
    - "/docs/2015/64-bit-firefox-for-windows-will-be-publicly-available-flash-is-only-supported-plug-in/"
---
Windows 向け Firefox 64 ビット版はしばらく前から [Developer Edition](https://www.mozilla.org/ja/firefox/developer/all/) と [Beta](https://www.mozilla.org/ja/firefox/beta/all/) でテスト用に公開されてきましたが、Firefox 42 以降、64 ビット版は [Release](https://www.mozilla.org/ja/firefox/all/) (安定版) チャンネルを通じて一般に公開されます。つまり、より多くのユーザーが 64 ビット版を使い始めるということで、あなたのサイトで提供しているコンテンツが 32 ビット版 [NPAPI プラグイン](https://developer.mozilla.org/ja/Add-ons/Plugins) を必要とする場合、それらの Firefox ユーザーは使用できないことになります。今のところ Adobe Flash Player が 64 ビット版で唯一の対応プラグインとなっています。コンテンツ提供者には、プラグインへの依存をやめ、[最新ウェブ技術](https://developer.mozilla.org/ja/docs/Web) を採用するよう強く推奨します。

**更新**: Mozilla が「パートナー関連のいくつかの変更を待っている」ため、Windows 64 ビット版の一般公開は延期されました。現時点でのスケジュールは不明です。

**更新**: Mozilla は Firefox 43 での 64 ビット版公開を決定しました。Silverlight 対応も有効化されています。

**更新**: 64 ビット版には、Flash コンテンツからファイルピッカーを開けないという [バグ](https://bugzilla.mozilla.org/show_bug.cgi?id=1236911) があります。Mozilla は Adobe と協力して問題の解決に取り組んでいます。
