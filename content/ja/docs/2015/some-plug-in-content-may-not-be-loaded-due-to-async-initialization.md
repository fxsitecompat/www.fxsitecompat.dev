---
title: "非同期初期化のため一部のプラグインコンテンツが読み込まれない可能性があります"
date: "2015-08-12T22:39:43-04:00"
categories: ["plugins"]
tags: []
versions: "40"
statuses: "reverted"
cclicense: "BY-SA 3.0"
references:
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1116806": "Bug 1116806 - Let Asynchronous Plugin Initialization ride the train"
    "https://bugzilla.mozilla.org/show_bug.cgi?id=1195607": "Bug 1195607 - Async Plugin Init compatibility issues found on release channel"
---
Firefox 40 では、Aaron Klotz が [ブログ記事](http://dblohm7.ca/blog/2014/06/17/asynchronous-plugin-initialization-an-introduction/) で説明している通り、パフォーマンス向上のため非同期のプラグイン初期化が有効化されました。この副作用として、Flash 動画や [*FarmVille 2*](https://bugzilla.mozilla.org/show_bug.cgi?id=1194958) といったゲームなど特定のプラグインコンテンツが、そのコード設計によっては正しく読み込まれない可能性があります。`about:config` で `dom.ipc.plugins.asyncInit` の設定値を `false` に変更して問題が再現しない場合、その問題は非同期初期化によるものです。開発者には、該当するプラグインベンダーに回避方法を問い合わせつつ、[バグを登録](https://bugzilla.mozilla.org/enter_bug.cgi?product=Core&component=Plug-ins&blocked=1195607) することをお勧めします。

**更新**: 相当数のサイトへ影響が及んだことから、この変更は <time datetime="2015-08-19">8 月 19 日</time> 更新の  [Firefox ホットフィックスアドオン](https://bugzilla.mozilla.org/show_bug.cgi?id=1196000) と <time datetime="2015-08-27">8 月 27 日</time> 公開の [Firefox 40.0.3](https://bugzilla.mozilla.org/show_bug.cgi?id=1198590) を通じてバックアウトされました。問題の [抜本的な解決策](https://bugzilla.mozilla.org/show_bug.cgi?id=1194600) が生み出され、Firefox 41 に実装されました。

**更新**: ホットフィックスアドオンとの競合を防ぐため、Firefox 41 で [設定名が変更され](https://bugzilla.mozilla.org/show_bug.cgi?id=1200698) `dom.ipc.plugins.asyncInit.enabled` になりました。既定値 (`true`) は変わりません。
