---
title: "Java に初期設定で Click-to-Activate が適用されます"
date: "2013-09-19T23:58:13-04:00"
categories: ["plugins"]
tags: []
versions: "26"
statuses: "affected"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=899080": "Bug 899080 – Make plugins default to click-to-play"
---
Firefox 26 以降、[プラグイン](https://developer.mozilla.org/ja/docs/Plugins) の有効化にはユーザインタラクションが必要となります。人気のある Adobe Flash Player を除き、Web ページに埋め込まれているすべてのプラグインコンテンツは初期設定で無効化され、ユーザのクリックで有効化されます。この変更は、ブラウザのセキュリティとパフォーマンスを向上させるために行われるものです。詳しくは [Mozilla Security Blog](https://blog.mozilla.org/security/2013/01/29/putting-users-in-control-of-plugins/) と [Future Releases Blog](https://blog.mozilla.org/futurereleases/2013/09/24/plugin-activation-in-firefox/) を参照してください。Web 開発者の皆さんには、[HTML5](https://developer.mozilla.org/ja/docs/Web/Guide/HTML/HTML5) をはじめとするモダンな Web 技術を活用して、より豊かなユーザ体験を提供することを推奨します。もしそれが不可能な場合は、[サイト作者のための Click-to-Activate プラグインガイド](https://developer.mozilla.org/ja/docs/Site_Author_Guide_for_Click-To-Activate_Plugins) を参照してください。

**更新**: Mozilla は、ホワイトリスト戦略が決定するまでの間、Beta と Release チャンネルでは、Java を除くすべてのプラグインの [Click-to-Activate 有効化を延期](https://bugzilla.mozilla.org/show_bug.cgi?id=941137) することを決定しました。
