---
title: "Flash プラグイン対応は 2020 年に廃止されます"
date: "2018-06-05T15:17:00-04:00"
categories: ["plugins"]
tags: []
versions: ["future"]
statuses: "affecting"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1455897"
      title: "Bug 1455897 - Remove support for the Flash plugin when Flash EOL's per the roadmap"
---
2017 年 7 月、[Adobe Systems](https://blogs.adobe.com/japan-conversations/201707adobe-flash-update/) は 2020 年末までに Flash Player プラグインの提供を終了することを発表し、それと同時に [Mozilla](https://blog.mozilla.org/futurereleases/2017/07/25/firefox-roadmap-flash-end-life/) は他のブラウザーベンダーとともに [Flash 対応ロードマップ](https://developer.mozilla.org/docs/Plugins/Roadmap) を更新しました。

現行のスケジュールによれば、Firefox は 2019 年前半に Flash を使用しているサイト上でユーザーに見える形での警告を表示し始め、その数か月後には Flash Player は初期設定で無効化されます。そして 2020 年前半には Firefox からプラグイン対応が完全に削除されますが、法人向けの Firefox 延長サポート版 (ESR) は 2020 年末まで対応を継続します。

デスクトップ版 Firefox は [Firefox 52](https://www.fxsitecompat.com/ja/docs/2016/plug-in-support-has-been-dropped-other-than-flash/) のリリースまでに他のすべての [NPAPI プラグイン](https://www.fxsitecompat.com/ja/categories/plugins/) 対応を打ち切っています。Android 版 Firefox は既に [Firefox 56](https://www.fxsitecompat.com/ja/docs/2017/flash-plug-in-is-no-longer-supported-by-firefox-for-android/) で Flash 対応を廃止しました。iOS 版 Firefox は WebKit ベースのため、元々ブラウザープラグインには対応していません。

まだ Flash に依存しているウェブサイトは、この最終期限を逃さないよう、しっかりした移行計画を立ててください。MDN の [Flash から HTML5 への移行ガイド](https://developer.mozilla.org/docs/Plugins/Flash_to_HTML5) には、このトピックに関するより詳しい情報が載っています。
